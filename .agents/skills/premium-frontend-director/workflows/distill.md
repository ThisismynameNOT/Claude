# Workflow: Distill

**Activates when**: the request is to reduce complexity, visual noise, duplication, or unnecessary animation while keeping the experience's intent intact — "this feels cluttered," "simplify this," "tone it down," "there's too much going on."

Distillation is not a downgrade — removing something that isn't earning its place is itself a craft decision, not a concession.

## Steps

1. Identify what the surface is actually trying to do (its mode and primary action, per [references/design-direction.md](../references/design-direction.md)) — distillation needs a target to cut toward, not just "less of everything."
2. Walk the surface and classify each element: load-bearing (removing it costs real information or function), reinforcing (supports the primary message but isn't essential), or decorative-only (adds visual activity with no informational or functional job).
3. Remove or simplify decorative-only elements first. For reinforcing elements, keep the ones that most directly support the primary action/message and cut or merge the rest.
4. Apply the same lens to motion specifically: any animation that doesn't pass the purpose-naming step in [references/motion-and-interactions.md](../references/motion-and-interactions.md) is a distillation target.
5. Re-run the critique stage from [references/review-and-audit.md](../references/review-and-audit.md) on the distilled result — cutting too far can flatten hierarchy as much as leaving too much can clutter it; distillation has an endpoint, not an unbounded direction.

## Guardrail

**Distinguish refinement/distillation from redesign.** A distill request is scoped to removing excess, not to replacing the underlying design language. If getting the clutter down genuinely requires restructuring the layout rather than trimming it, say so and confirm before doing a structural redesign under a "simplify" request.

## Acceptance criteria

- Every element removed is traceable to "decorative-only" or "non-essential reinforcing," not a guess.
- The primary action/message is at least as clear after distillation as before.
- Nothing load-bearing (information or function) was cut.
- The result still passes the mandatory quality gates in SKILL.md.
