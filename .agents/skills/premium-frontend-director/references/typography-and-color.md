# Typography and color

## Typography

- Choose typefaces for product character, language coverage, legibility, and performance. Do not reject a familiar family if it is the right fit.
- Build a clear hierarchy for page titles, section headings, body, labels, metadata, and code or numbers when present.
- Use line length, line height, weight, and spacing to support reading rather than relying on size alone.
- Use fluid type only where interpolation improves responsive behavior; retain sensible minimum and maximum sizes.
- Check all required languages, diacritics, numerals, and fallback behavior. For Czech or Slovak, test accented glyphs in every selected face and weight.
- Load only used weights/styles. Prefer local/system or properly subsetted assets when appropriate; avoid blocking the page on optional decorative faces.
- Keep text selectable and preserve zoom/reflow.

## Color

Define semantic roles such as page, surface, text, muted text, border, action, success, warning, and error. Choose relationships between roles, not isolated swatches. Make status understandable without color alone.

Check contrast for text, controls, focus indicators, and essential graphical information against the applicable WCAG success criteria. Test actual rendered combinations, including hover, disabled, dark/light, and image overlays. Do not assume a palette is accessible because its color values look far apart.

Dark mode is an option, not a universal requirement. Use it only when it suits the product and can be implemented consistently across surfaces, images, states, charts, and embedded content.

## Tokens

Use existing tokens first. If adding tokens, name them by semantic use rather than by one component or screenshot (for example, `text-muted` rather than `gray-600` when the codebase supports semantic tokens). Avoid changing global values for a local adjustment without checking its impact across routes.

## Verification

Inspect type and color at mobile and desktop sizes, at browser zoom, with real content, and in the relevant language. Use tools such as a contrast checker as support; combine them with human inspection of hierarchy and legibility.
