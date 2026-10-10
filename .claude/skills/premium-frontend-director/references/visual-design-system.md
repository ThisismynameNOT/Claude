# Visual design system

## Build a coherent system

Create or extend a small set of decisions that the interface can reuse: color roles, type roles, spacing rhythm, container and grid rules, shape/border treatment, elevation, icon style, and motion tokens when needed. Store them in the project's existing system or format. Avoid parallel token systems that disagree.

Start with the actual information and task, then choose the right hierarchy. A system should make repeated decisions consistent while allowing a one-off composition where it improves clarity.

## Composition and hierarchy

- Make the primary action or content unmistakable.
- Group related information; separate unrelated priorities.
- Vary scale, placement, and rhythm when meaning calls for it.
- Use whitespace intentionally; avoid empty space that hides needed controls.
- Use cards only when containment or comparison is meaningful.
- Preserve reading order across visual rearrangement.
- Give repeated sections a common rhythm without making every section identical.

## Component language

Define component states, not just their default appearance: idle, hover, focus, pressed, selected, disabled, loading, success, empty, and error as applicable. Keep labels, icons, border treatment, spacing, and state transitions consistent. Use the established component library when it fits; customize visual defaults where needed without breaking its accessibility contract.

| Component family | Design and behavior checks |
|---|---|
| Navigation, menus, buttons, links | Distinguish actions from navigation; show current location and focus; make mobile and keyboard paths complete. |
| Forms, search, filters | Label inputs; retain user values through errors; make applied filters and clear/reset actions visible; persist state in the URL when useful. |
| Cards, tables, results | Use containment only when meaningful; keep table headers, sort state, row actions, and dense-data reflow understandable. |
| Dialogs, drawers, dropdowns | Define opening/closing, focus entry/return, Escape behavior, outside click behavior, and scroll handling. |
| Tabs, accordions | Keep selected/expanded state visible and keyboard behavior consistent with the chosen pattern. |
| Galleries, carousels | Provide controls and a clear current position; avoid autoplay unless required and controllable; retain touch and keyboard access. |
| Notifications, loading, empty, error states | Communicate what happened, what is happening, or what to do next; use non-color cues and accessible status announcements where appropriate. |

Prefer native HTML for common controls. For complex widgets, use a mature accessible component implementation or follow an established keyboard pattern. See [accessibility and usability](accessibility-and-usability.md).

## Images and visual assets

Use images to communicate relevant content, not to fill a decorative slot. Match crop and aspect ratio to subject matter. Set dimensions or aspect ratios to reduce layout shifts. Verify usage rights and provenance; use a clearly marked placeholder when source media is unavailable.

## Distinction from a redesign

For a refinement, preserve the incumbent visual language except within scope. For a redesign, inspect the incumbent to understand product content and behavior, then choose a replacement direction that fits the brief. Do not blend in fragments of the old look simply because they already exist.
