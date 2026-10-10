# Layout and responsive behavior

## Let content determine the layout

Choose grid, columns, container width, and breakpoints from content and interaction needs. Avoid forcing one breakpoint system across unrelated pages when the project already has established rules. Use CSS grid/flexbox and intrinsic sizing before adding viewport-specific exceptions.

Maintain logical source order. If visual order changes at a breakpoint, ensure keyboard and screen-reader reading order remains coherent. Keep navigation, action controls, and form labels available at narrow widths without relying on hover.

## Plan responsive states

Inspect at least one narrow phone, one intermediate or breakpoint-adjacent width, and one wide desktop for ordinary frontend work. When responsive rules are part of the change or a visual release gate, use the supplied matrix as a default sample: 320, 375, 390, 768, 1024, 1280, and 1440 CSS pixels. Add widths when a real breakpoint, content edge, or device class requires them.

At each chosen width check:

- overflow, clipping, overlap, and text wrapping;
- navigation and visible primary action;
- line length and heading scale;
- image crop and layout stability;
- touch reach and target spacing;
- dense data, tables, and long labels;
- sticky or fixed elements obscuring content.

Do not claim a width was tested unless it was actually rendered or inspected.

## Reflow and input

Support browser zoom and text growth. Let controls wrap or stack instead of shrinking tap targets or clipping labels. Provide a non-hover path for hover content. Do not assume every touch device is small or every desktop device has a mouse; use capability queries only when they improve interaction.

## Images and media

Use responsive sources and appropriate dimensions when the stack supports them. Give important images useful alternative text; mark purely decorative images accordingly. Preserve focal subjects at all breakpoints. Avoid autoplay or heavy media that blocks the main task.

## Layout acceptance

Accept a responsive layout when content remains readable, controls remain operable, task priority remains clear, and no important content is hidden or overlapped at the checked widths. Record the actual widths and devices inspected.
