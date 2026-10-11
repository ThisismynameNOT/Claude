# Workflow: Implement Reference

**Activates when**: the user supplies a concrete visual reference — a screenshot, a Figma file, an existing site, a written spec — and wants it reproduced, not reinterpreted. "Implement this exactly," "build this from the screenshot," "match this design."

This workflow inverts the normal priority order: **fidelity to the supplied reference outranks this Skill's own design-direction and default-avoidance guidance.** Don't apply the "avoid Inter/Fraunces as defaults" or "avoid 3-equal-column rows" guidance here if the reference itself uses them — reproducing the reference faithfully is the actual job.

## Steps

1. Extract the reference's actual values, not an impression of them: exact or closely-matched colors, type (measure/compare against common faces if the exact one isn't named), spacing, breakpbehavior if visible, and interaction/motion if it's a live reference rather than a static image.
2. Confirm scope: pixel-exact reproduction, or reproduction adapted to a different stack/framework while keeping the same visual result? If genuinely ambiguous, ask once; otherwise assume "same visual result, idiomatic implementation for the target stack."
3. Build it against the project's actual stack and constraints ([references/frontend-engineering.md](../references/frontend-engineering.md)) — fidelity to the reference, not necessarily to the reference's original implementation technique.
4. Still apply, even here: accessibility baseline ([references/accessibility-and-usability.md](../references/accessibility-and-usability.md)) and the production-grade engineering baseline — a faithfully reproduced design still needs semantic markup, keyboard operability, and working forms, none of which a static screenshot can show. If the reference is visibly inaccessible (e.g., unreadable contrast), say so and ask whether to preserve it exactly or correct it.
5. Verify against the reference directly — side-by-side at matching viewport, not just "looks about right."
6. **Respect copyright and asset ownership.** Don't reproduce a reference that's a competitor's branded design as if it were this user's own brand; flag that distinction if it looks like it might be happening.

## Acceptance criteria

- The build matches the supplied reference's actual values, not this Skill's general-purpose defaults.
- Accessibility and engineering baselines still hold even though visual direction deferred to the reference.
- Any place the implementation had to deviate from the reference (because of inaccessibility, a different stack, or ambiguity in the source) is stated explicitly, not silently decided.
