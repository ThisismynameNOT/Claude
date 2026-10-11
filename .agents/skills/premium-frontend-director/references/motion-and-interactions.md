# Motion and Interactions

Primary source: Emil Kowalski's animation philosophy, independently verified against current browser/API behavior. Motion should feel physically believable, purposeful, and interruptible — never decoration bolted on after the fact.

## Decision framework — run this before writing any animation

1. **Why does this animation exist?** If you can't name a reason, don't build it.
2. **What triggers it** — a user action or a system state change?
3. **What does it communicate** — feedback, spatial origin/destination, a state change, or bridging a jarring content swap?
4. **Does it improve spatial understanding**, or is it decorative?
5. **Can it be interrupted or reversed** mid-flight without glitching?
6. **Does it create a performance or accessibility risk** (main-thread cost, motion sickness, distraction from a frequent task)?
7. **Would a simpler solution be better** — an instant state change, a static affordance?

### Frequency gate

| Frequency | Decision |
|---|---|
| 100+ times/day (keyboard shortcuts, command-palette toggle) | No animation. This is a disqualifier, not a judgment call. |
| Tens of times/day (hover, list navigation) | Near-imperceptible only, or nothing |
| Occasional (modals, drawers, toasts) | Standard animation |
| Rare/first-time (onboarding, success, celebration) | The delight budget lives here |

## Tool selection — cheapest that works

| Need | Tool |
|---|---|
| Hover/press/color/state toggle driven by a class or attribute | CSS transition |
| Entry animation on mount, no JS state | CSS `@starting-style` |
| Predetermined motion that must stay smooth while the page is busy | CSS `@keyframes` animation (runs off the main thread) |
| Programmatic control with CSS-level performance, no library | WAAPI (`element.animate()`) |
| Springs, layout animations, exit animations, gesture-driven values | A motion library (Motion/Framer Motion, React Spring, etc.) |
| Full-page scrolltelling, scroll-pinned sequences | GSAP + ScrollTrigger, isolated in its own component |
| 3D/canvas backgrounds and scenes | Three.js/WebGL, isolated in its own component |

Don't install a motion library dependency for a single fade. Isolate GSAP/Three.js/canvas work in dedicated leaf components with proper mount/unmount cleanup — mixing a scroll-hijacking library and a spring-based UI library in the same component tree is a real, frequently-hit source of competing-rAF bugs, not a stylistic preference.

## Properties

- Animate `transform` and `opacity` by default — both skip layout and paint and run on the compositor. Animating `width`/`height`/`top`/`left`/`margin`/`padding` forces layout recalculation on every frame and is the most common cause of janky UI motion; avoid it except where there's no transform equivalent (accordion open/close is the standard exception, and even there a `grid-template-rows: 0fr → 1fr` or a measured-height approach is often smoother than raw `height`).
- `clip-path` is a reasonable fourth property for reveal effects — also compositor-friendly in modern browsers.
- Never `scale(0)` as an entrance — nothing in the physical world appears from literally nothing. Start around `scale(0.92-0.97)` + `opacity: 0`.
- Anchor `transform-origin` at the trigger element for popovers, dropdowns, menus, and tooltips. Modals are the exception — they're not spatially anchored to a trigger, so keep them centered.
- Prefer percentage-based `translate()` (relative to the element's own size) over hardcoded pixel offsets for things like off-screen positioning.
- In JS-driven animation, animate the full `transform` string/property rather than separate `x`/`y`/`scale` shorthands where the library's shorthand isn't itself compositor-optimized — check the library's own docs, since this varies by library and version; don't assume last year's advice still applies without checking.

## Easing and duration

Use named, consistent curves rather than inventing a `cubic-bezier()` per component:

```css
--ease-out: cubic-bezier(0.23, 1, 0.32, 1);        /* entering/exiting elements */
--ease-in-out: cubic-bezier(0.77, 0, 0.175, 1);    /* moving/morphing on screen */
--ease-standard: ease;                              /* hover/color transitions */
/* linear for constant motion: marquees, progress bars */
```

Avoid `ease-in` on UI motion — a slow start delays the exact moment the user is watching for feedback; `ease-out` reads as faster even at an identical duration.

| Element | Duration |
|---|---|
| Button press feedback | 100-160ms |
| Tooltips, small popovers | 125-200ms |
| Dropdowns, selects | 150-250ms |
| Modals, drawers | 200-500ms |
| Marketing/explanatory sequences | can run longer — justify the length against the point it's making |

Most interface motion should stay under ~300ms; longer UI animations read as sluggish rather than deliberate, with marketing/storytelling sequences as the explicit exception.

## Springs

Reach for a spring (rather than a duration/easing pair) when motion involves drag-with-momentum, something that should feel alive and physical, a gesture the user can interrupt or reverse mid-flight, or decorative pointer-tracking effects:

```js
{ type: "spring", duration: 0.5, bounce: 0.2 }            // perceptual params — easier to reason about
{ type: "spring", mass: 1, stiffness: 100, damping: 10 }   // physical params — more precise control
```

Keep bounce around 0.1-0.3 for most UI; save higher bounce for drag-to-dismiss and explicitly playful moments.

## Interruption, exit, and gesture handoff

- Use transitions, not keyframe animations, for anything a user can trigger more than once in quick succession (toasts, toggles) — transitions retarget smoothly from the current value, keyframes restart from zero and visibly stutter on re-trigger.
- Springs inherently carry velocity through an interruption — a released drag should hand its exit velocity into the settle animation rather than snapping to a fixed duration from a standstill. This is the core of what makes iOS-style interfaces feel physically continuous.
- Exit the way something entered — a toast sliding up from the bottom should also leave through the bottom; symmetric paths make swipe-to-dismiss and hide/reveal feel obvious rather than arbitrary.
- Use asymmetric timing where the user is actively deciding: slow and deliberate on a hold-to-confirm press, snappy on the system's response once released.

## Premium/iOS-inspired interaction character (optional, not a visual identity to copy)

Interaction *quality* and *brand identity* are separate decisions — none of the following implies copying Apple's visual language:

- Precise tactile feedback on every interactive element (press states are not optional polish, they're baseline).
- Deliberate acceleration/deceleration rather than linear or default-easing motion for anything that should feel physical.
- Spatially coherent transitions — things move from where they visually are to where they're going, not teleporting or fading in a generic spot.
- Interruptible, reversible gestures wherever a drag or swipe is involved.
- Consistent transform-origins so related elements always expand/collapse from the same logical point.
- Clear, visible focus and selection states — distinct from hover.

## Accessibility — ships with the animation, not after

```css
@media (prefers-reduced-motion: reduce) {
  .element { animation: fade 0.2s ease; } /* keep opacity/color changes, drop transform-based movement */
}
@media (hover: hover) and (pointer: fine) {
  .element:hover { transform: scale(1.05); } /* gate hover so touch taps don't fire false hover states */
}
```

Reduced motion means fewer and gentler animations, not zero — preserve transitions that aid comprehension (a state change still needs to be legible), remove ornamental movement and large position changes. Account for touch devices (gesture equivalents for drag-only interactions), keyboard users (every animated interactive element still operable via keyboard with a visible focus state), and pointer capability. Essential content or functionality must never require an animation to be understood or reached.

## Never ship

| Never | Instead |
|---|---|
| `transition: all` | Name the exact properties |
| `transform: scale(0)` entrance | `scale(0.92-0.97)` + `opacity: 0` |
| `ease-in` on UI motion | `ease-out` or a named custom curve |
| An invented, one-off `cubic-bezier()` per component | The project's shared easing tokens |
| Animation on a keyboard shortcut or 100+/day action | No animation |
| `window.addEventListener('scroll', ...)` driving animation | Scroll-linked hooks, `IntersectionObserver`, or CSS `animation-timeline: view()` |
| A `requestAnimationFrame` loop writing to framework state every frame | Motion-value-style primitives that bypass render |
| Everything entering the viewport at once | A 30-80ms stagger |
| Missing `prefers-reduced-motion` handling above `MOTION_INTENSITY` 3 | A gentler variant, not zero |
