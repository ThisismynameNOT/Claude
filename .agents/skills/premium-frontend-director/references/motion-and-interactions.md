# Motion and interaction design

## Decide whether motion belongs

For every non-trivial animation, name its purpose: feedback, state indication, spatial continuity, prevention of a jarring transition, explanation, or rare delight. If it serves none, omit it. Frequency is a useful heuristic: highly repeated work actions need fast, low-distraction feedback; occasional transitions can use more spatial explanation.

Never make essential information or task completion depend on motion. Keep focus, content, and controls stable when users read or act on them.

## Choose the smallest suitable tool

- Use CSS transitions for simple state changes.
- Use CSS keyframes for predetermined sequences.
- Use Web Animations API or existing project primitives when programmatic control is needed.
- Use an established motion library for spring physics, layout transitions, exit handling, or gesture control when those needs justify it.
- Reuse the project's tokens and dependencies before adding a library.

These are choices, not prohibitions. Browser support, interruption behavior, framework conventions, and the measured performance profile determine the final tool.

## Shape the transition

Specify the trigger, start/end states, timing/curve, origin, interruption or reversal behavior, and cleanup. Keep movement proportional to the spatial relationship. Use opacity/transform when they express the effect and profile well; do not pretend every animation must avoid layout or paint work. Reduce large, repeated, parallax, and pointer-following effects when they distract or cost too much.

For drag and gesture interactions, provide a clear alternative and preserve a stable target. For shared-element or layout transitions, make the source/destination relationship legible and prevent jumps when content changes. For scroll-linked reveals, ensure content remains available if animation is unsupported or reduced. For route transitions, preserve meaningful focus, title, and navigation state. Gate pointer-following effects away from coarse input and never rely on them to reveal essential information.

For a sophisticated sequence, prefer the library already present in the project. Motion or GSAP may fit orchestration, gesture, or timeline needs; neither should be added for a trivial fade. Optional tactile or spring-like behavior can influence interaction feel without copying Apple's branding.

## Input and accessibility

- Check `prefers-reduced-motion`; remove or substantially reduce non-essential movement while retaining state feedback.
- Support keyboard, touch, and pointer. Never make an essential action hover-only.
- Avoid trapping focus or moving focus unexpectedly when visual content animates.
- Ensure drag or gesture interactions have a simple alternative where users must complete an action.
- Do not flash or create motion likely to trigger discomfort.

See [MDN: prefers-reduced-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/%40media/prefers-reduced-motion) for implementation details.

## Verify

Test entrance and exit, repeated activation, interruption, reduced motion, keyboard operation, and touch behavior. Profile only when the experience or task warrants it; state whether the result is measured or visually estimated.
