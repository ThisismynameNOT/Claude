# Layout and Responsive Design

## Composition

- **Responsive grid architecture** — a real grid system (CSS Grid or a utility framework's grid), not ad hoc absolute positioning.
- **Asymmetry when purposeful** — justified by content weight or hierarchy, not decoration for its own sake. At higher `DESIGN_VARIANCE`, asymmetric layouts (offset overlaps, mixed aspect ratios, fractional-unit grids) collapse to a strict single column below ~768px regardless of level.
- **Editorial composition** — large type and generous negative space as the layout itself, when the mode (Read/Experience) and brief call for it.
- **Section rhythm and visual pacing** — vary section height and density deliberately rather than repeating one template block down the page.
- **Alignment systems** — pick a consistent alignment logic (edge-aligned, centered, baseline-grid) and keep it; wandering alignment reads as unintentional.
- **Container widths, whitespace, information density** — tie to `VISUAL_DENSITY` from the design brief.
- **Section transitions and visual storytelling** — how one section hands off to the next (a color shift, an overlap, a full-bleed break) should feel considered, especially on Persuade/Experience surfaces.
- **Content hierarchy** — one clear primary action/message per section; avoid competing focal points.

## Patterns to default away from (not ban)

These are over-represented defaults, not forbidden patterns — use them when they are genuinely the right tool, state that choice, and don't reach for them reflexively:

- **The identical 3-equal-column feature-card row** as the default way to present three features. A 2-column zigzag, an asymmetric grid, a scroll-pinned sequence, or a horizontal-scroll strip are alternatives worth considering — but if the user explicitly wants three equal cards, or it's genuinely the clearest layout for the content, build it. See the priority hierarchy.
- **Zigzag alternation beyond 2 consecutive rows** — a third left/right-alternating row in a row starts to feel mechanical; break the pattern or vary the row content/size instead.
- **An eyebrow label above every section** — keep eyebrows to roughly 1 per 2-3 sections so they retain meaning; skip section-number eyebrows (`00 / INDEX`, `002 · Capabilities`) in favor of plain-language labels.
- **Decorative structural elements with no function** — hairline crosshair grids, rotated vertical agency-portfolio text, bottom-of-hero decoration strips (`BRAND. MOTION. SPATIAL.`) — fine when they organize real content or carry real navigation, generic when added purely to "feel designed."
- **Scroll cues** (`Scroll ↓`, animated mouse-wheel icons) — usually unnecessary; a visible partial element at the fold communicates "more below" without a label.
- **Decorative colored status dots** on nav items, list rows, or badges with no real state behind them.

## Responsive behavior

- Design and verify at minimum: 320, 375, 390, 768, 1024, 1280, 1440px.
- Navigation collapses to a real mobile pattern (sheet, drawer, or simple stacked menu) with working focus management and Escape-to-close — not a desktop menu just shrunk.
- Touch targets ≥ 44×44px (iOS HIG) / 48×48dp (Material) on touch-capable viewports.
- Images and media reflow without cropping out the subject; use `object-fit` and art-direction (`<picture>`/`srcset`) rather than one fixed aspect ratio forced everywhere.
- No horizontal scroll/overflow at any tested width unless it's an intentional horizontal-scroll component (and even then, the page itself shouldn't overflow).
- Verify real user journeys at each breakpoint (can the primary action actually be completed on a 375px-wide screen with one hand), not just that the layout doesn't break.

## Section/z-index hygiene

Keep z-index to a documented, small scale reserved for genuinely systemic layers (sticky nav, modal/overlay, toast, grain/texture overlay). Avoid scattering arbitrary `z-10`/`z-50` values through component code as a reflexive fix for stacking issues — trace the actual stacking context instead.
