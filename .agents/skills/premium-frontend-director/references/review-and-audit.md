# Review and audit

## Five review passes

1. **Craft:** verify concept, task hierarchy, information architecture, and feasibility before implementation.
2. **Critique:** inspect whether the interface communicates, differentiates, and uses decoration or repetition deliberately.
3. **Audit:** inspect functionality, accessibility, responsiveness, performance, content accuracy, and engineering contracts.
4. **Polish:** fix meaningful details in type, spacing, alignment, image crop, interaction, focus, and motion.
5. **Distill:** remove anything that adds noise, latency, maintenance, or cognitive load without supporting the intended experience.

Treat the passes as a checklist, not an obligation to rewrite every page. A small refinement may need one targeted critique and a bounded check.

## Evidence-based findings

Record each finding with:

- **Severity:** critical, high, medium, or low.
- **Evidence:** exact route, state, viewport, reproduction steps, or tool output.
- **Impact:** who or what task is affected.
- **Recommendation:** a specific correction.
- **Confidence:** observed, inferred, or unverified.

Use critical for a security, data, or core-task failure; high for a major access or workflow block; medium for substantial friction or repeated visual breakage; low for localized polish. Adjust severity to actual consequence and explain the reason.

## Bounded visual QA

When rendering tools exist, inspect desktop and mobile together in one pass. Check representative routes and interaction states. Fix observed defects in a batch, then use one confirmation pass. Continue only if a concrete failure remains or the user requests broader verification; do not create an endless polish loop.

Check horizontal overflow, clipped text, layout changes, focus, keyboard operation, touch, forms, empty/loading/error states, console output, reduced motion, and actual primary journeys. Use the viewport matrix in [layout-and-responsive](layout-and-responsive.md) when appropriate.

## Scores and hard failures

Use [quality-rubric](../evaluations/quality-rubric.md) only when a score helps compare or communicate readiness. Cite evidence for each rating. Mark unobserved categories unscored instead of guessing. A weighted average never cancels a critical functional, security, factual, or accessibility failure.

## Stop conditions

Do not call work finished while a known critical issue remains. If a test is unavailable, state the exact limitation and the smallest next check needed. Do not say “fully accessible,” “production ready,” or “passes Core Web Vitals” without evidence for that claim.
