# Accessibility and usability

## Target and honesty

Use WCAG 2.2 Level AA as a practical target when applicable. This is a target, not an automatic conformance claim. A successful automated scan does not prove conformance; combine automated checks with manual keyboard, zoom/reflow, content, and assistive-technology checks appropriate to the product.

## Semantics and navigation

- Use native headings, landmarks, lists, buttons, links, labels, and form controls.
- Keep heading levels and page structure meaningful.
- Use ARIA only when native HTML does not provide the necessary semantics; match role, state, keyboard behavior, and focus model.
- Keep a visible focus indicator and a logical focus order. Do not remove outlines without an equivalent.
- Support keyboard operation for all essential controls. For custom widgets, follow the relevant WAI-ARIA APG keyboard pattern instead of improvising.
- Ensure focus is not obscured by sticky headers, dialogs, or overlays.

## Content and controls

- Give controls clear accessible names and state. Make the purpose clear in text, not icon shape alone.
- Associate labels, instructions, and errors with form fields. Identify errors and explain how to correct them.
- Provide status feedback for important async actions without stealing focus unnecessarily.
- Preserve text zoom/reflow and user settings. Do not communicate status by color alone.
- Provide keyboard alternatives to dragging and pointer-only interactions where appropriate.
- Respect reduced-motion preferences; avoid flashes and distracting movement.

## Usability and states

Make the main task and next action clear. Prevent avoidable errors, preserve user input when validation fails, and provide recovery for destructive or irreversible actions. Design loading, empty, success, error, disabled, and unavailable states when the task can reach them.

## Practical review

Test keyboard-only navigation, focus visibility and order, labels and errors, zoom/reflow, contrast, touch interaction, reduced motion, and representative assistive technology when available. Record tools and limitations. Use [WCAG 2.2](https://www.w3.org/TR/WCAG22/) as the normative success-criteria reference and [WAI-ARIA APG](https://www.w3.org/WAI/ARIA/apg/) for informative widget patterns.
