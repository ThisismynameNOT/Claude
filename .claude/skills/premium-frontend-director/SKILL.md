---
name: premium-frontend-director
description: Design, build, redesign, refine, animate, implement references for, and audit websites or web application interfaces. Use for frontend UI, visual systems, responsive design, interaction, accessibility, performance, and production-quality implementation; do not use for backend-only work.
---

# Premium Frontend Director

Help deliver distinctive, usable, responsive, accessible, authentic, and technically sound frontend work. Treat visual polish as a result of deliberate decisions, not a count of effects.

## Operating priorities

Resolve decisions in this order:

1. The user's stated requirements and approved constraints.
2. Factual accuracy, security, legal obligations, and accessibility.
3. Existing behavior, project architecture, and technical contracts.
4. User needs and product goals.
5. A coherent design system and implementation quality.
6. Optional stylistic conventions.

Inspect existing code, routes, assets, content, and patterns before changing an established product. Keep verified facts separate from assumptions. Do not fabricate business claims, client work, testimonials, credentials, staff, addresses, or performance results. Do not replace a framework, CMS, API, or major dependency without a clear reason and authorization.

## Route the request

Choose the closest workflow and combine modes only when the request needs it:

| Request | Workflow | Common interface mode |
|---|---|---|
| Create a new frontend | [create](workflows/create.md) | Persuade, Operate, Read, or Experience |
| Replace an existing visual direction | [redesign](workflows/redesign.md) | Infer per surface |
| Make a bounded improvement | [refine](workflows/refine.md) | Preserve incumbent mode |
| Add or improve animation | [animate](workflows/animate.md) | Any mode; motion is contextual |
| Review quality and defects | [audit](workflows/audit.md) | Infer per surface |
| Reproduce a supplied visual reference | [implement-reference](workflows/implement-reference.md) | Match the reference |
| Reduce complexity or visual noise | [distill](workflows/distill.md) | Preserve product purpose |

Use these interface modes as lenses, not templates:

- **Persuade:** marketing, landing pages, and product presentation.
- **Operate:** dashboards, CMS, settings, and task-focused tools.
- **Read:** editorial, documentation, and information-heavy content.
- **Experience:** image-led, spatial, or narrative presentation.

Apply a different mode to different routes or components when useful.

## Core sequence

1. **Understand:** identify audience, task, business goal, constraints, source assets, required states, localization, and success evidence. Ask only for information that blocks a sound decision; otherwise record a reasonable assumption.
2. **Direct:** define a compact design brief before coding: concept, hierarchy, type and color direction, composition, imagery, interaction, motion, responsive strategy, and one project-specific signature detail. Never reuse a signature motif across unrelated products by default.
3. **Build:** extend the existing stack and tokens where practical. Use semantic HTML, accessible native controls, maintainable components, and functioning routes, forms, and states.
4. **Verify:** when browser or screenshot tools exist, render representative desktop and mobile views, inspect interactions and console output, fix observed defects, then perform one bounded confirmation pass. Expand the viewport matrix when responsive rules change. Never claim unperformed visual, accessibility, or performance tests.
5. **Deliver:** summarize the direction, changed behavior, verification evidence, assumptions, and unresolved items.

## Optional design dials

Use only when they help the brief. Accept user-provided 1–10 values; otherwise infer silently or state a short assumption when it affects the result.

- `DESIGN_VARIANCE`: conventional composition to more experimental composition.
- `MOTION_INTENSITY`: little motion to more expressive motion.
- `VISUAL_DENSITY`: spacious information layout to dense information layout.

These dials do not measure quality and never override the user's brief, usability, accessibility, brand fit, or project constraints.

## Load only relevant guidance

Read the workflow first, then load the references needed for the request:

- Design intent or mode choice: [design-direction](references/design-direction.md), [visual-design-system](references/visual-design-system.md).
- Type, color, or composition: [typography-and-color](references/typography-and-color.md), [layout-and-responsive](references/layout-and-responsive.md).
- Motion: [motion-and-interactions](references/motion-and-interactions.md), [accessibility-and-usability](references/accessibility-and-usability.md).
- Business, portfolio, or localized content: [content-and-brand-authenticity](references/content-and-brand-authenticity.md).
- Implementation, SEO, or speed: [frontend-engineering](references/frontend-engineering.md), [performance-and-seo](references/performance-and-seo.md).
- Review or acceptance: [review-and-audit](references/review-and-audit.md), [quality-rubric](evaluations/quality-rubric.md).
- Representative task patterns: [examples](examples/).

## Completion gates

Before calling work complete:

- Preserve user constraints, routes, content, integrations, and existing behavior outside scope.
- Confirm every visible control has a meaningful action or is clearly non-interactive.
- Check narrow and wide layouts, keyboard operation, focus visibility, form errors, loading and empty states when relevant.
- Respect `prefers-reduced-motion`; do not make essential meaning depend on animation.
- Verify external claims and asset rights or mark them as placeholders requiring review.
- Separate measured evidence from estimates. Report critical failures regardless of any quality score.

Use [activation tests](evaluations/activation-tests.md) to evaluate routing and [quality rubric](evaluations/quality-rubric.md) only when a structured score is useful.
