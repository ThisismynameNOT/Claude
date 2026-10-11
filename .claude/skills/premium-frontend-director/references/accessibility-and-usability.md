# Accessibility and Usability

Accessibility is a dedicated audit pass (see [review-and-audit.md](review-and-audit.md) and [workflows/audit.md](../workflows/audit.md)), not a running commentary during design. Checking it constantly while designing tends to produce timid, over-cautious layouts; checking it rigorously at a dedicated stage catches real issues without flattening the work.

## Baseline target

WCAG 2.2 AA across the board; AAA contrast target for hero/display copy where feasible.

## Structural

- Semantic HTML first: real `<button>`, `<a>`, `<nav>`, `<main>`, `<header>`, `<form>` elements — not `<div onClick>` standing in for interactive controls.
- One `<h1>` per page; heading levels don't skip (no `<h2>` straight to `<h4>`).
- Landmark regions (`<main>`, `<nav>`, `<footer>`) so screen-reader users can jump between sections.
- A visible skip-to-content link as the first focusable element.

## Keyboard

- Every interactive element reachable and operable via keyboard alone, in a logical tab order that matches visual order.
- Visible focus states on everything focusable — distinct from hover, never `outline: none` without a replacement.
- Modals/drawers trap focus while open and return focus to the trigger on close; Escape closes them.
- Custom components (tabs, comboboxes, menus) implement the expected keyboard pattern (arrow keys, Home/End, type-ahead) and correct ARIA roles — don't reinvent a pattern a native element or an accessible library already solves correctly.

## Screen reader and assistive tech

- Meaningful `alt` text on informative images; empty `alt=""` on purely decorative ones.
- Form inputs have associated, visible `<label>` elements (not placeholder-as-label).
- Error messages are programmatically associated with their field (`aria-describedby`) and announced.
- Dynamic content changes (toasts, live search results, loading completion) use `aria-live` appropriately — not every update, just the ones a sighted user would also notice.
- Icon-only buttons have an accessible name (`aria-label` or visually-hidden text).

## Touch and pointer

- Touch targets at least 44×44px (iOS) / 48×48dp (Material) with adequate spacing between adjacent targets.
- Hover-only affordances have a touch/focus equivalent — nothing is *only* reachable by hovering.
- Gesture-only interactions (swipe-to-dismiss, drag-to-reorder) have a non-gesture alternative.

## Cognitive load and usability

- One primary action per view/section; secondary actions visually subordinate.
- Error messages are specific and actionable ("Card number must be 16 digits" not "Invalid input").
- Destructive actions (delete, cancel subscription) require confirmation or are easily undoable.
- Forms show inline validation as the user completes fields, not only on submit.
- Loading and empty states explain what's happening and what to do next rather than leaving a blank or ambiguous screen.

## Usability isn't separate from accessibility

A usability failure (a confusing error message, an undiscoverable primary action, inconsistent navigation) degrades the experience for everyone and disproportionately for users already working harder to use the interface. Treat the two as one review pass, run together in [workflows/audit.md](../workflows/audit.md).
