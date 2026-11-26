# Anti-Slop Taste Rules, Image-to-Code & Web Interface Guidelines

> Sub-module for `PRISM` uniting Taste Skill 2.5.1's 9 House Rules, Image-to-Code token extraction, and Vercel Web Interface accessibility/UX checks.

---

## 1. The 9 Anti-Slop House Rules (Non-Negotiable)

1. **No captions under images/renders**: Put credits on one clean footer line if required.
2. **Zero empty grounds**: Every visual slot renders real photography, real UI, or crisp vector art across `1440`, `1024`, `768`, and `390`.
3. **One section per screen**: Hero owns screen 1 at `1440x900` with no next heading peeking in; keep sections 1–2 screens tall.
4. **Equal left/right edges**: Align all content strictly to shared `.wrap` / grid tracks.
5. **Restrained hover micro-animations**: Linked cards lift `2px`, photos zoom `1.02–1.03`, crisp hero entrance — no cheesy 3D card tilt, auto-carousels, or timed tabs.
6. **Real visuals over fake icons**: Use real photography or authentic product UI; crisp vector icons (`lucide` / clean SVG) without blurry gradients.
7. **Tech effects for tech brands only**: Classify business kind (`software`, `gaming`, `tech`, `product`, `service`, `place`). Dark glassmorphism, shaders, and WebGL belong strictly to `software`/`gaming`/`tech`; physical places/services get real photography + flat clean grounds.
8. **Clean contact hygiene**: Use sanitized `.example` domains and non-sensitive placeholders for mock forms/footers.
9. **Break repetitive template defaults**: Avoid endless centered dark heroes or alternating text/image zigzags unless the layout genuinely calls for it.

---

## 2. Image-to-Code Token Extraction (Mockup -> Production Code)

- **Measure First, Code Second**: Inspect reference screenshots via `read_file` to extract layout zones, max-width, column count, spacing rhythm, hex palette (`bg`, `surface`, `ink`, `muted`, single `accent`), and type pairing/weights before writing markup.
- **No Cards-Inside-Cards-Inside-Cards**: Flatten nested rounded containers, fake telemetry pills, and decorative status dots.
- **Never Embed Whole Mockups**: Implement real interactive semantic HTML/React/Tailwind matching the extracted tokens (never drop a full UI screenshot as a static `<img>`).

---

## 3. Web Interface Guidelines & Playwright Live Check

Before shipping any web UI:
- **Accessibility & Interaction**: Semantic landmarks (`header`, `main`, `nav`, `footer`), visible `:focus-visible` rings, full keyboard navigation, `>= 4.5:1` body text contrast, `>= 44x44px` mobile tap targets, and `prefers-reduced-motion` support.
- **PowerShell/Windows Verification**: Serve locally and verify live rendered views across desktop (`1440x900`) and mobile (`375x812` / `390x844`) via Playwright CLI or Chrome DevTools MCP with zero console/network errors.
