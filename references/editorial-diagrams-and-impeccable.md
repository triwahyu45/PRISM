---
name: editorial-diagram-design
description: Creates publication-grade self-contained HTML+SVG editorial diagrams (no shadows, no Mermaid slop, 52 diagram archetypes) and provides Impeccable design critique/polish verbs (polish, bolder, quieter, critique, audit, distill, clarify, delight) for frontend UI and explainer video visuals.
---

# Editorial Diagram Design & Impeccable UI Craft

Combines **Editorial Diagram Design** (`diagram-design`) for crisp, publication-grade HTML+SVG diagrams with **Impeccable** (`impeccable`) critique and polish steering verbs for frontend interfaces and motion visuals.

---

## 1. Editorial Diagram Craft (`diagram-design`)

Generate diagrams as a **single self-contained HTML + SVG file** — zero blurry drop shadows, zero generic Mermaid slop, and crisp export to SVG/PNG or direct embedding in Remotion/explainer videos.

### Visual Laws
- **Flat Crisp Strokes**: Use clean `1.5px–2px` lines, sharp arrowheads, and subtle `1px` structural borders instead of heavy box shadows or gradients.
- **Strict 3-Color Brand Palette**: 1 canvas background, 1 primary ink (`#111827` or `#F8FAFC`), and 1 bold accent color for active nodes/callouts.
- **Typography & Whitespace**: Pair a clean grotesk sans (`Inter`, `Geist`, `Plus Jakarta Sans`) with `JetBrains Mono` for labels/metrics; keep `>= 25%` breathing room around node groups.

### 6 Core Diagram Families (52 Archetypes)
1. **Flows & Pipelines**: Linear process, branching decision tree, swimlane, feedback loop, state machine.
2. **Hierarchies & Trees**: Org chart, taxonomy tree, mind map, dependency DAG.
3. **Comparisons & Matrices**: 2×2 quadrant, feature matrix, before/after split, spectrum bar.
4. **Timelines & Roadmaps**: Horizontal milestone track, Gantt, version evolution, beat sheet.
5. **Architecture & Systems**: Layered stack, client-server sequence, event bus, data lineage.
6. **Data & Proportional**: Sankey/flow bars, concentric rings, waffle/dot grid, callout anatomy.

---

## 2. Impeccable Design Steering Verbs (`impeccable`)

Scale craft to the surface's **Mode**:
- **Persuade / Experience** (landing pages, promos, hero showcases): Commit to a bold, distinct visual POV.
- **Operate / Read** (dashboards, docs, forms, tools): Prioritize precision, restraint, and zero visual friction.

### Action Verbs
- **`polish`**: Tighten alignment, spacing rhythm, optical margins, and micro-interactions.
- **`bolder`**: Increase typographic contrast, scale jump, and accent commitment when UI feels generic.
- **`quieter`**: Strip redundant borders, badges, and visual noise when UI feels loud.
- **`critique`**: Audit hierarchy, copy clarity, user flow, and visual balance before coding fixes.
- **`audit`**: Check accessibility, contrast, responsive breakpoints, and edge cases (empty/loading/error states).
- **`distill` / `clarify`**: Cut unnecessary steps or jargon so the primary value lands in 3 seconds.
- **`delight`**: Add purposeful spring motion or tactile hover feedback without hurting performance.

Always verify rendered UI/diagrams visually at target viewport sizes before finalizing.
