# Performance

## Core Web Vitals as real targets, not decoration

- **LCP (Largest Contentful Paint) < 2.5s** — the hero image/text block should load with priority (`priority`/`fetchpriority="high"`/preload), not compete with below-fold assets.
- **INP (Interaction to Next Paint) < 200ms** — keep heavy computation off the main thread; debounce/throttle expensive handlers; avoid large synchronous work in response to input.
- **CLS (Cumulative Layout Shift) < 0.1** — reserve space for images, embeds, ads, web fonts, and any async-loaded content before it arrives.

## Measurement discipline

**Distinguish measured results from estimated or theoretical performance, every time.** If Lighthouse, WebPageTest, or real browser DevTools were actually run, report the real numbers. If they weren't available in the environment, say so plainly and give the user instructions to run them, rather than stating confident-sounding numbers that were never measured. This matters as much as the numbers themselves — a fabricated "95/100 Lighthouse score" is worse than an honest "not measured in this environment, here's how to check."

## Practical levers

- **Images**: correct sizing/format for their actual render size (don't ship a 4000px image into a 400px slot), modern formats with fallback, lazy-loading below the fold, explicit `width`/`height` to prevent shift.
- **Fonts**: `font-display: swap`/`optional`, subset to the needed character set where practical, limit the number of weights/families actually loaded.
- **JavaScript**: code-split by route, lazy-load anything not needed for the initial render (heavy motion libraries, 3D/canvas work, below-fold interactive widgets), avoid shipping an entire icon library when a handful of icons are used.
- **CSS**: avoid unused utility bloat where it's easy to prevent (tree-shaking/purging in build tooling); keep specificity sane so overrides don't cascade into !important chains.
- **Third-party scripts**: load analytics/chat-widget/marketing-pixel scripts `async`/`defer` and as late as reasonably possible; each one is a real, measurable cost to INP and LCP.
- **Rendering strategy**: use static generation or server rendering where the framework supports it for content that doesn't need to be client-rendered on every load; reserve full client-side rendering for genuinely interactive/stateful surfaces.

## When performance and visual ambition trade off

Say so explicitly rather than silently picking one side. A hero-scale WebGL scene and a sub-1s LCP are in real tension; name the trade-off, offer the lighter-weight alternative (a static hero with a smaller interactive element below the fold, a video loop instead of a live 3D scene), and let the user decide if the brief doesn't already settle it.
