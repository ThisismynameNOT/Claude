# Activation and behavior scenarios

Use these prompts with the skill enabled and record which skill/workflow activates. These are evaluation cases, not claimed execution results.

## Should activate

1. **Construction site:** “Build a Czech website for this construction company using only these approved services and real project photos.” Expected: create; Persuade plus Experience; authenticity and localization guidance.
2. **Photography:** “Redesign this photographer portfolio around the supplied gallery and preserve the booking form.” Expected: redesign; Experience plus Persuade; image rights and form-contract checks.
3. **Dashboard:** “Make this dense operations dashboard easier to use on mobile without slowing repeated actions.” Expected: refine or redesign based on scope; Operate; responsive/accessibility guidance and restrained motion.
4. **Animation:** “Add a brief state transition when this filter finishes loading.” Expected: animate; decide if feedback improves understanding; reduced motion and keyboard state remain.
5. **Audit:** “Audit the public site for mobile layout, keyboard, and form issues; don't change anything.” Expected: read-only audit with evidence, severity, and unrun checks.
6. **Reference fidelity:** “Implement the attached product page screenshot at 1440px and tell me where you could not match it.” Expected: implement-reference; fidelity priority; actual comparison evidence.
7. **Distillation:** “Remove visual clutter from this page but keep the existing identity and all actions.” Expected: distill; preserve identity and contracts.

## Should not activate

1. “Write a SQL migration to add a table; there is no frontend.” Expected: no activation.
2. “Explain what a CSS grid is conceptually.” Expected: no implementation workflow unless the user asks to work on an interface.
3. “Review this API's authentication design; no user interface is involved.” Expected: no activation.

## Fidelity and integrity checks

- A refinement prompt must not produce an unrequested redesign.
- An exact reference prompt must not be overridden by a preferred art direction.
- A real-company prompt with missing facts must not produce invented credentials or testimonials.
- A request involving motion must include an accessible no-motion path.
- A requested audit must not silently edit files or site state.

## Recording template

For each run, record prompt, selected workflow/mode, supporting files loaded, whether expected constraints were honored, and one observed failure or “none observed.” Do not infer activation quality from the description alone; run examples in the target Claude surface.
