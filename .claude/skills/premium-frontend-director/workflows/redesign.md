# Workflow: Redesign

**Activates when**: replacing the visual system of an existing site/app while preserving its business content and required functionality — "redesign this," "modernize this," "give this a new look."

## Steps

1. **Audit the current site before touching it.** Document: brand tokens in use (colors, fonts, logo treatment, radii), information architecture (page tree, nav, conversion paths), content blocks (what exists, what's doing work, what's filler), patterns worth preserving (a signature interaction, recognizable hero, established copy voice), patterns worth retiring (generic templates, broken layouts, dead links, perf traps), and an inferred current reading of the dials (`DESIGN_VARIANCE`/`MOTION_INTENSITY`/`VISUAL_DENSITY`) as the actual starting point, not an assumed baseline.
2. **Capture the SEO baseline** — current ranking pages, meta titles, structured data, OG cards. SEO regression is the single biggest risk in a redesign; treat it as a protected contract per [references/frontend-engineering.md](../references/frontend-engineering.md).
3. **Determine scope with the user if genuinely ambiguous**: *preserve* (modernize without breaking the existing brand — evolve gradually) vs. *overhaul* (new visual language on top of the same content and IA, old look treated as evidence/anti-reference rather than a constraint). If the brief already states this, don't ask — proceed.
4. Run SKILL.md Steps 2-4 (mode, dials, design brief) treating the current site's audit as real input, not a blank slate.
5. **Apply modernization levers in priority order**, stopping once the brief is satisfied rather than always going to the end of the list: (1) typography refresh — biggest lift per unit of risk, (2) spacing/rhythm, (3) color recalibration (desaturate/unify neutrals, keep the brand accent), (4) motion layer added to existing components, (5) hero/key-section recomposition, (6) full block replacement — only when the existing block is genuinely unsalvageable.
6. **Protect what should never change silently**: URL/route structure, primary nav labels, form field names/order, the logo/wordmark, existing legal/consent copy, analytics event names. Changing any of these is a decision for the user, not a side effect of a visual refresh.
7. Run the full verification loop from [references/review-and-audit.md](../references/review-and-audit.md), including a direct before/after comparison of the protected items in step 6.

## Decision: targeted evolution vs. full redesign

- IA, content, and SEO are sound → targeted evolution (levers 1-4 above). Most of the value, least of the risk.
- Visual debt is structural (broken IA, no design system, broken mobile) → full redesign, with strict content preservation.
- The brand itself is changing → treat as [create.md](create.md), informed by the audit as historical record rather than as a constraint.

## Acceptance criteria

- The pre-redesign audit actually happened and is referenced in the decisions made.
- Nothing in step 6's protected list changed without explicit confirmation.
- The result reads as a coherent evolution (or deliberate overhaul) of this specific business, not a generic template applied over its content.
