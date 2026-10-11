# Workflow: Create

**Activates when**: building a new site/app/surface from a brief, with little or no existing implementation to preserve.

## Steps

1. Run SKILL.md Steps 1-4 in full: understand the project, set mode(s), set the dials, write the internal design brief — including the signature visual element. Don't skip to code with an implicit brief in your head; make the decisions explicit so later critique/audit stages have something concrete to check against.
2. Choose the stack per [references/frontend-engineering.md](../references/frontend-engineering.md) — honor any constraint the user already stated (framework, hosting, CMS); otherwise pick the simplest stack that serves the brief.
3. Build information architecture before visual design: page/section list, primary nav, the one or two primary actions per page.
4. Build the design system first (tokens: type scale, color, spacing, radii, motion curves/durations) then compose pages from it — not the reverse. This is what keeps 6+ sections from drifting into visually unrelated blocks.
5. Build real content where it's available (see [references/content-and-brand-authenticity.md](../references/content-and-brand-authenticity.md)); mark placeholders explicitly where it isn't.
6. Implement with the production-grade baseline from [references/frontend-engineering.md](../references/frontend-engineering.md) — don't treat accessibility, responsive behavior, or error handling as a later pass bolted onto a "done" visual build.
7. Run the full verification loop: [references/review-and-audit.md](../references/review-and-audit.md) — visual QA at all viewports, then the five-stage craft → critique → audit → polish → distill pass.

## Acceptance criteria

- The internal design brief exists and the shipped build matches it (or deviations are explained).
- No mandatory quality gate (SKILL.md) is failing.
- The signature visual element is actually specific to this project, not a repeated house move.
- QA ran and was reported honestly, including what wasn't verifiable in this environment.
