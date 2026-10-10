# Add or improve motion

## Inputs

Use the target interaction, current implementation, input methods, frequency of use, and user motion preferences.

## Procedure

1. Decide whether motion adds useful feedback, state indication, spatial continuity, explanation, or suitable rare delight. If not, recommend a static alternative.
2. Identify trigger, start/end state, frequency, interruption/reversal behavior, and reduced-motion behavior.
3. Use the simplest existing project tool that meets the need. Check [motion and interactions](../references/motion-and-interactions.md); avoid new dependencies for simple effects.
4. Implement only the relevant movement and states. Keep repeated work actions fast and predictable; keep essential information readable and stable.
5. Test keyboard, pointer, touch, reduced motion, repeated activation, and interruption when relevant. Inspect runtime errors and performance if the effect is complex.

## Deliver

State the motion's purpose, tool choice, reduced-motion behavior, and checks performed.

## Acceptance

- Motion communicates something useful and can be completed without motion.
- It does not hide essential content, block input, steal focus, or require hover.
- Reduced motion is supported and verified when tools allow.
