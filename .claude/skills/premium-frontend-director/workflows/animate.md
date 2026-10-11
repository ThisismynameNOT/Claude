# Workflow: Animate

**Activates when**: adding or fixing motion/interaction without redesigning the underlying layout. "Add some motion to this," "this transition feels janky," "make this feel more alive."

## Steps

1. Load [references/motion-and-interactions.md](../references/motion-and-interactions.md) in full.
2. For each element in scope, run the decision framework from that file **in order**: should it animate at all (frequency gate) → what's the purpose → cheapest tool that fits → which properties → easing/duration or spring → interruption/exit handling → reduced-motion and pointer gating. The frequency gate is the most commonly skipped step and the one most likely to produce an animation that shouldn't exist — don't skip it because motion was explicitly requested; "add motion" still means "add motion where it earns its place."
3. If an existing animation is the complaint (feels slow, janky, abrupt), diagnose against the "Never ship" table in [motion-and-interactions.md](../references/motion-and-interactions.md) before reaching for a bigger fix — most janky motion is animating the wrong property (layout-triggering instead of transform/opacity) or using keyframes where a transition was needed.
4. Implement, then self-check against the same "Never ship" table.
5. Verify `prefers-reduced-motion` actually degrades correctly and hover effects are gated behind `(hover: hover) and (pointer: fine)`.

## Output format (matches the source philosophy's own discipline)

After implementing, report in a few lines, not a long writeup:

- **The gate result** — frequency tier and the named purpose. If something was rejected by the gate, say which and why.
- **The ingredients** — tool, properties, easing/duration or spring config, one line each.
- **What needs a feel-check** — anything that can't be judged from the code alone (a spring's bounce, a crossfade's balance) — name the specific thing to look at, not a blanket "please review."

## Acceptance criteria

- Every animated element passed the frequency gate explicitly — including a documented "no, don't animate this" where that was the right call.
- No "Never ship" item from [motion-and-interactions.md](../references/motion-and-interactions.md) is present.
- Reduced-motion and hover-gating are in place wherever required.
- The underlying layout/structure is unchanged unless the user also asked for that.
