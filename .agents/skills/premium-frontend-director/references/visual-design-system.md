# Visual Design System and Components

Every component should read as part of one coherent design language defined by the design brief (tokens for color, type, radius, spacing, shadow, motion) — not as a grab-bag of defaults from whatever library was convenient.

Component libraries (shadcn/ui, Radix, Material, Fluent, Carbon, Polaris, etc.) are acceptable and often correct, especially for Operate-mode surfaces where native expectations and accessibility matter more than novelty. **Never ship a component library's out-of-the-box visual defaults unexamined** on a Persuade/Experience surface that needs a distinctive identity — adapt radii, color, shadow, and type to the project's tokens.

## Coverage checklist (apply what's relevant to the project)

- **Navigation** — primary nav, mobile nav pattern, in-page anchors/table of contents for long Read content, breadcrumbs for deep Operate hierarchies.
- **Buttons** — primary/secondary/tertiary hierarchy, loading state, disabled state, real press feedback (see motion-and-interactions.md).
- **Cards** — consistent internal padding/rhythm, a clear clickable area if the whole card is a link, hover state that doesn't fight the page's motion budget.
- **Forms** — label placement, inline validation, error messaging (see also content-and-brand-authenticity.md for copy), accessible required-field marking, logical tab order.
- **Modals and drawers** — focus trap, Escape-to-close, click-outside behavior, centered (modals) vs. edge-anchored (drawers) with the animation origin to match.
- **Dropdowns, select, combobox** — keyboard operable (arrow keys, type-ahead, Escape), anchored and positioned to stay on-screen.
- **Galleries and carousels** — real keyboard/swipe support, visible position indicator, pause-on-hover/focus for autoplay, and an escape from autoplay entirely for accessibility.
- **Tabs and accordions** — correct ARIA roles (`tablist`/`tab`/`tabpanel`, `button[aria-expanded]`), content reachable without JS where feasible.
- **Search and filters** — visible active-filter state, an obvious way to clear filters, empty-result state that suggests a next step.
- **Tables** — for dense data, a real table element or table-semantics component (not div-grids pretending to be tables) with sortable-column affordances where relevant.
- **Notifications/toasts** — don't steal focus, auto-dismiss with a reasonable timeout or persist for errors, announce via `aria-live` for screen readers.
- **Loading states** — skeletons that match the real content's shape, not a generic spinner for anything that takes longer than ~300ms; nothing longer than ~300ms with zero loading indication.
- **Empty states** — explain why it's empty and what to do next, not just "No results."
- **Error states** — specific, actionable, and in the product's own voice — see content-and-brand-authenticity.md.

## Consistency check

Before calling a component system done, scan for: multiple one-off button styles that should be the same component, inconsistent corner radii across cards/inputs/buttons, spacing values that don't belong to the declared scale, and icon sets mixed from more than one family.
