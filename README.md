# PRISM — Web Motion, Editorial SVG Diagrams & UI Craft

AI Agent Skill for **Antigravity**, **Claude Code**, and **OpenAI Codex**. Complete frontend craft suite: frame-by-frame animation cloning (`reanimate`), 52 self-contained HTML+SVG diagram archetypes, Impeccable UI critique/polish, GSAP 3 + ScrollTrigger, Karpathy surgical coding rules, and live DevTools QA.

---

## Quick Install (Claude Code / Codex / Antigravity)

Clone this skill into your agent's global or project skills directory:

| Agent | Global Install Path | Project-Local Path |
| :--- | :--- | :--- |
| **Antigravity** | `~/.gemini/config/skills/PRISM` | `.agents/skills/PRISM` |
| **Claude Code** | `~/.claude/skills/PRISM` | `.claude/skills/PRISM` |
| **OpenAI Codex** | `~/.codex/skills/PRISM` | `.agents/skills/PRISM` |

```bash
# Example (Antigravity / Claude Code / Codex — pick your path):
git clone https://github.com/triwahyu45/PRISM.git ~/.claude/skills/PRISM
```

---

## Requirements & Dependencies (For Agents)

- **Runtime / Tools**: **Node.js 18+** / browser runtime for web builds; **Chrome / Playwright** for live visual QA
- **MCP Servers**: Recommended: `chrome-devtools` MCP (or Playwright) for live desktop/mobile screenshot & CLS/console verification
- **Related Skills**: None required
- **API Keys / Secrets**: None

```json
{
  "mcpServers": {
    "chrome-devtools": {
      "command": "npx",
      "args": ["-y", "chrome-devtools-mcp@latest"]
    }
  }
}
```

---

## Included Files

- `SKILL.md` — Frontend craft loop & visual QA gate
- `references/editorial-diagrams-and-impeccable.md` — 52 SVG diagram archetypes & UI polish verbs
- `references/gsap-motion-design.md` — GSAP 3, ScrollTrigger, & `@gsap/react` patterns
- `references/reanimate-and-devtools-qa.md` — Frame-by-frame motion cloning & LCP/CLS QA
- `references/karpathy-coding-rules.md` — Surgical diff & anti-over-engineering rules
- `references/taste-and-web-guidelines.md` — Taste 9 rules, Image-to-Code tokens, & Web Interface accessibility checks

## When to Trigger / Search Keywords

`prism`, `ui polish`, `svg diagram`, `editorial diagram`, `gsap`, `scrolltrigger`, `reanimate`, `clone animation`, `frontend qa`, `karpathy`
