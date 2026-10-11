# Typography and Color

## Typography

**Choose typefaces for purpose, not familiarity.** A font is not "safe" because it's common and not "bad" because it's common — Inter is a perfectly good interface font for a product that genuinely wants an invisible, neutral UI typeface; it is a tell only when picked by default without considering whether the brief wants something more distinctive. Likewise a display serif (Fraunces, Instrument Serif, Playfair) is excellent for editorial/luxury/publication work and wrong for a SaaS dashboard. **Pick the face that fits this brief**, and if the brand already has a typeface, keep it — don't swap a locked brand font for a "more interesting" one.

When nothing is specified, default away from the two most over-represented AI-generated-site choices (Inter as the only typeface in the system, Fraunces/Instrument Serif as the only display face) **as defaults**, not absolutes — if the user asks for Inter, use Inter.

Cover, as relevant to the project:
- **Optical hierarchy** — size, weight, and color carry hierarchy together; don't rely on size alone (avoid oversized H1s that just shout).
- **Type scale and line height** — a deliberate scale (e.g. a modular ratio or a small hand-picked set), with line-height tuned per size band (tighter for display, ~1.5 for body).
- **Letter spacing** — slightly negative on large display sizes, neutral-to-slightly-positive on all-caps labels.
- **Line length** — body copy around 45-75 characters per line.
- **Fluid typography** — `clamp()`-based sizing for display type where it genuinely improves responsiveness, not as a default for every element.
- **Font loading performance** — `font-display: swap` or `optional`, subset where practical, self-host or use `next/font`/equivalent rather than a blocking third-party `<link>`.
- **Glyph coverage** — verify the chosen face covers the target language(s), especially for non-Latin scripts or accented characters.
- **Editorial vs. interface typography** — a Read/Experience surface can carry a distinct, larger-personality type system from an Operate surface in the same product; don't force one type system everywhere a product has multiple modes.

## Color

- **Brand-led palettes** — start from the client's actual brand color if one exists; invent a palette only for greenfield work with no existing brand.
- **Semantic tokens** — name colors by role (`--surface`, `--surface-elevated`, `--text-primary`, `--accent`, `--danger`) rather than hard-coding hex values through components.
- **Tonal hierarchy and neutral relationships** — a coherent neutral ramp (not just black/white/one-gray), with surfaces distinguished by subtle elevation rather than hard borders everywhere.
- **Contrast and accessibility** — WCAG AA minimum for body text, AAA target for hero/large copy; verify, don't eyeball.
- **Light and dark themes** — build both **only when the product actually benefits from it**: most consumer apps and many marketing sites do; a print-emulating editorial piece or a brand whose identity depends on one exact palette may not. Evaluate per project rather than defaulting to "always ship both." When both are built: pick one token strategy (CSS variables or a utility-framework dark variant) and keep it consistent; avoid pure `#000000`/`#ffffff` (near-black/near-white preserve depth); keep hierarchy parity and brand-accent recognizability across both modes; respect `prefers-color-scheme` as the default unless the brand insists on one mode.
- **Avoid default-AI tells as defaults, not absolutes**: an ungrounded purple-gradient brand color with no basis in the brief, neon outer glows as the default elevation technique, and oversaturated accents that fight the neutral palette. None of these are banned outright — a brief that specifically wants a bold neon aesthetic should get one.

## Resolving a typography/color conflict

If the user's brief and this file's defaults disagree, the brief wins (priority hierarchy, SKILL.md). This file exists to fill gaps the brief leaves open and to catch unexamined defaults, not to overrule stated intent.
