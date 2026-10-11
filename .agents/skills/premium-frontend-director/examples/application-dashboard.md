# Example: Professional SaaS Dashboard (Operate mode)

## Brief

"A dashboard for our platform — dense data, needs to feel fast and precise, not flashy."

## How the Skill should work it

**Mode**: Operate throughout (even if the product's own marketing site elsewhere is Persuade — this surface is a different mode and gets different priorities).

**Dials**: `DESIGN_VARIANCE` low (1-3: predictable grid, consistent card/table structure — unpredictability here costs users time, it doesn't read as creative). `MOTION_INTENSITY` low (1-3: state transitions and feedback only, no decorative motion — see the frequency gate in [references/motion-and-interactions.md](../references/motion-and-interactions.md); a dashboard is opened dozens of times a day, which disqualifies most "delight" motion outright). `VISUAL_DENSITY` high (7-9: tight padding, tabular numerics, information-dense tables/cards, minimal decorative whitespace).

**Critical correction vs. a generic build**: do not inherit marketing-page motion defaults (parallax, scroll reveals, hover-tilt cards) onto this surface just because they were used elsewhere in the product. Operate-mode motion is almost entirely feedback and state-indication — see [references/motion-and-interactions.md](../references/motion-and-interactions.md)'s purpose list; "delight" is reserved for the rare/first-time tier (onboarding, a genuine milestone), not routine dashboard use.

**Components**: lean on an accessible, native-feeling component library (per [references/visual-design-system.md](../references/visual-design-system.md)) rather than hand-building complex interactive patterns (comboboxes, data tables, date pickers) from scratch — correctness and keyboard behavior matter more than novelty here.

**Accessibility**: this is the mode where [references/accessibility-and-usability.md](../references/accessibility-and-usability.md) matters most in practice — users doing repeated daily tasks disproportionately benefit from full keyboard operability, consistent focus order, and predictable interaction patterns.

**Brand**: still present, but "in precise details" rather than as a dominant visual move — the brand's accent color used correctly in data visualization, the type system reused from the main brand but tuned for data density, consistent iconography. Not a diluted version of the marketing site's visual language.

## What "done" looks like

Fast perceived performance (skeleton states matching real content shape, no unnecessary loading spinners for sub-300ms operations), full keyboard operability including complex components (tables, filters, comboboxes), minimal-but-present brand expression, and zero motion that would annoy a user opening this dashboard for the fifth time that day.
