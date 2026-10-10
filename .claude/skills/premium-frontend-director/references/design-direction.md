# Design direction

## Understand before styling

For a new or substantially changed surface, identify the product or business, audience, main task, business outcome, content, brand, source assets, constraints, integrations, locales, and evidence that will define success. Inspect the existing code and current UI when available. Label missing facts as assumptions; ask only when a missing fact blocks a consequential decision.

## Select the interface mode

Use one or several modes as reasoning tools, not templates:

- **Persuade:** make value, credibility, and the next action legible.
- **Operate:** optimize task completion, state awareness, error recovery, and information density.
- **Read:** support scanning, comprehension, long-form attention, and navigation through information.
- **Experience:** let imagery, sequence, space, or interaction carry the story without compromising access to content.

Choose per page or component. A marketing site can include an Operate-style booking flow; an editorial product can use Experience on a cover and Read for its articles.

## Form the design brief

Before implementation, define in a short note:

1. Concept and reason it suits this product.
2. Hierarchy and visual identity.
3. Type, color, and composition.
4. Image, material, or data treatment.
5. Interaction and motion language.
6. Responsive behavior and accessibility considerations.
7. One distinctive detail tied to real product or brand meaning.

For a narrow change, keep this brief internal and brief. Do not turn a one-field correction into a full creative process.

## Use the dials carefully

`DESIGN_VARIANCE`, `MOTION_INTENSITY`, and `VISUAL_DENSITY` can help translate a user preference into a rough direction. Treat each 1–10 value as an ordinal preference, not a measurement or automatic generator. A user-given number is a constraint to consider; it never licenses poor contrast, inaccessible interaction, generic imitation, or excessive motion.

As optional orientation, 1–3 usually signals restrained/low, 4–7 balanced/contextual, and 8–10 expressive/high. For example, `DESIGN_VARIANCE: 2` may favor a conventional editorial grid while `8` may allow purposeful asymmetry; `MOTION_INTENSITY: 2` may use brief state feedback while `8` may add occasional expressive transitions; `VISUAL_DENSITY: 2` may create spacious storytelling while `8` may suit a data-heavy dashboard. These are starting examples, not universal recipes.

If no values are given, infer from the audience, task, brand, and existing product. Do not force the user to choose numbers.

## Originality without novelty theater

Differentiate through real content, deliberate hierarchy, distinctive composition, material/imagery choices, and interaction fit. Avoid repeated hero-plus-three-cards patterns when they do not fit; use them when they are the clearest solution. Do not add gradients, blur, glow, glass, asymmetry, or animation just to signal “premium.”

Do not imitate a brand's protected identity. An interaction reference such as “tactile” or “spatial” may guide behavior without copying its visual identity.

## Validate direction

Check that the concept:

- serves the primary task before adding atmosphere;
- is supported by available content and assets;
- can be expressed in the existing stack and schedule;
- works in narrow, wide, keyboard, and reduced-motion contexts;
- has a recognizable reason for its visual signature.

If the user gives a precise design reference, use [implement-reference](../workflows/implement-reference.md) and prioritize fidelity over this skill's stylistic preferences.
