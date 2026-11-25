# Reanimate Motion Cloning & Chrome DevTools QA

## 1. Frame-by-Frame Motion Cloning (`reanimate`)
When rebuilding an animation from a live site, MP4, GIF, or Lottie reference:
1. Capture the reference at fixed viewport & FPS (`reanimate/scripts/capture.ts`).
2. Extract CSS/WAAPI timelines, WebGL draw calls, or fit exact cubic-bezier/spring curves (`easing.ts`).
3. Implement in clean React/GSAP/CSS (`transform` & `opacity` only — zero layout reflow).
4. Re-capture your copy and run frame-by-frame comparison (`compare.ts` / `sheet.ts`) until timings match.

## 2. Chrome DevTools Visual, A11y & Core Web Vitals QA
Before shipping any web UI or interactive page:
- Inspect live DOM & console/network errors via Chrome DevTools MCP (`chrome-devtools-plugin`).
- Verify LCP, CLS (zero layout shift on animated hero/scroll triggers), keyboard navigation, and mobile viewport (`375×812`) rendering.
