# Reanimate Motion Cloning & Chrome DevTools QA

## 1. Frame-by-Frame Motion Cloning (`reanimate`)
When rebuilding an animation from a live site, MP4, GIF, or Lottie reference:
1. **Pick Fidelity Level First**:
   | Level | Must Match | May Differ |
   | :--- | :--- | :--- |
   | **motion-faithful** *(default)* | Trigger, sequence, stagger, timing (±80 ms), easing family, relative travel, proportions | Copy, colors, fonts, images, brand details |
   | **pixel-faithful** | Everything above + fonts, sizes, colors, spacing, radii, shadows, assets; mean frame mismatch ≤ 2% | Nothing unrequested |
   | **mixed** | Cloned parts at one of the levels above | User-requested additions |
2. **Capture Reference & Canvas/WebGL**:
   - Capture at fixed viewport & FPS (`reanimate/scripts/capture.ts`).
   - For Canvas, WebGL, WebGPU, or Three.js/Pixi/Spline scenes: pass `--clock virtual --gl --assets` and inspect `gl/summary.md` & `gl/shaders/` directly (never rebuild shaders from screenshots alone).
3. **Extract & Implement**:
   - Extract CSS/WAAPI timelines, WebGL draw calls, or fit exact cubic-bezier/spring curves (`easing.ts`).
   - Implement in clean React/GSAP/CSS (`transform` & `opacity` only — zero layout reflow).
4. **Verify & Iterate (Max 5 Rounds)**:
   - Re-capture your copy with identical viewport/crop/trigger and run frame-by-frame comparison (`compare.ts` / `sheet.ts`) until every spec row passes.

### 9 Pitfalls That Waste Rounds
- **Mismatched viewport or crop** between reference and clone: fix capture before touching code.
- **Judging first & last frames only**: easing lives in the middle frames — read every filmstrip sheet.
- **Font fallback mismatch**: load the exact font from `inspect.json` for pixel-faithful work, or ignore text pixels and inspect timing columns for motion-faithful work.
- **Loaded page vs cold clone**: use `--wait-before` or `--trigger none` + `--pre-js` to restart animations cleanly.
- **Scroll-driven motion**: compare per `scrollY` using identical `--scroll-steps` and `--scroll-ms`, not per second.
- **GSAP / Framer springs**: `--playback-rate` does not slow JS springs — tune overshoot and settle time using `track.json` + `easing.ts`.
- **Screen-recording noise**: crop browser chrome/cursors and raise `--pixel-threshold` (~0.15).
- **Non-deterministic WebGL/Canvas**: always capture both sides with `--clock virtual` and the same `--seed`.
- **Guessing shaders**: read `gl/shaders/` and constant uniforms from the trace first.

## 2. Chrome DevTools Visual, A11y & Core Web Vitals QA
Before shipping any web UI or interactive page:
- Inspect live DOM & console/network errors via Chrome DevTools MCP (`chrome-devtools-plugin`).
- Verify LCP, CLS (zero layout shift on animated hero/scroll triggers), keyboard navigation, and mobile viewport (`375×812`) rendering.
