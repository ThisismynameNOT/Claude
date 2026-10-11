# Design Direction

Loaded for Step 1-4 of SKILL.md: understanding the project and writing the internal design brief before any code.

## 1. Understand the project

Gather, in order of how much they change the output:

1. **Business/product identity** — what it actually is, not a category guess. A "construction company" spans civil engineering, residential renovation, and industrial fabrication; each wants a different visual language.
2. **Industry and competitive environment** — what the category's existing sites look like, so the result can differentiate on purpose rather than by accident.
3. **Target customers and their needs** — who arrives, what they're trying to decide or do.
4. **Primary business objective** — a lead form, a purchase, a signup, a read-through, a task completed.
5. **Primary user actions** — the 1-3 things most visitors should actually do.
6. **Brand personality** — in adjectives the client would recognize, not generic ones ("precise and understated" beats "modern and professional").
7. **Available visual materials** — real photography, logos, existing brand assets.
8. **Existing design constraints** — a design system, brand guidelines, locked colors/fonts.
9. **Required functionality** — forms, auth, search, commerce, CMS-driven content.
10. **Technical constraints** — framework, hosting, CMS, existing codebase.
11. **Accessibility, performance, localization requirements.**

For an existing project, inspect the actual codebase, design tokens, and documentation before proposing anything — don't redesign from a blank mental slate when real constraints exist.

**Distinguish verified information from assumptions.** When something is unverifiable (a claimed stat, a client name, a completed project), say so and don't present it as fact. Ask for clarification only when the missing piece is essential and genuinely unguessable (e.g., "do you have a logo file, or should I typeset the name"); otherwise make a reasonable, clearly-labeled provisional decision and continue. Don't block on questions a competent director would just decide.

## 2. Interface modes

Classify **each surface**, not the product as a whole:

| Mode | Visitor's job | Typical surfaces | Priorities |
|---|---|---|---|
| **Persuade** | Decide and act | Landing pages, marketing sites, pricing, campaigns, product presentation | Differentiation, emotional register, clear conversion path |
| **Operate** | Complete a task | Dashboards, CMS/admin, settings, productivity tools, editors | Scanability, consistency, native platform expectations, speed over expression |
| **Read** | Understand something | Docs, articles, reports, changelogs, help centers | Structure for comprehension first, then a reading experience worth staying in |
| **Experience** | Be inside the work | Photography/architecture portfolios, galleries, immersive showcases | The artifact leads; the interface recedes |

A single product routinely spans modes: a SaaS tool's own landing page is Persuade even though its in-app surfaces are Operate; a fashion house's documentation is still Read even though its storefront is Persuade. Pick the mode from the surface in front of you.

## 3. Design parameters (the dials)

`DESIGN_VARIANCE`, `MOTION_INTENSITY`, and `VISUAL_DENSITY` (1-10 each) are starting points inferred from brief + mode, not fixed rules — see SKILL.md Step 3 for the bands. Typical defaults by mode: Persuade skews mid-to-high variance and motion; Operate skews low variance, low-to-mid motion, mid-to-high density; Read skews low variance and motion, low-to-mid density; Experience skews high variance, mid-to-high motion, low density. Override freely when the brief says otherwise — these are priors, not constraints (see the priority hierarchy in SKILL.md: user requirements outrank dial defaults).

## 4. The internal design brief

Write this out (even briefly, in your own working notes or a short preamble) before touching implementation code:

1. **Design concept and rationale** — the one-sentence idea and why it fits this business.
2. **Visual identity** — the overall look in a few concrete reference points, not mood-board adjectives alone.
3. **Typography strategy** — see [typography-and-color.md](typography-and-color.md).
4. **Color system** — see [typography-and-color.md](typography-and-color.md).
5. **Composition and layout strategy** — see [layout-and-responsive.md](layout-and-responsive.md).
6. **Image and material direction** — what real or placeholder imagery communicates, and its treatment (crop, grain, duotone, none).
7. **Interaction language** — how things respond to being touched: snappy and mechanical, soft and springy, quiet and restrained.
8. **Motion language** — see [motion-and-interactions.md](motion-and-interactions.md).
9. **Responsive behavior** — what changes shape vs. what just reflows.
10. **Signature visual element** — one element meaningfully tied to this company's actual identity: an architecture firm might communicate structural layering or construction sequencing; a photographer might lead with image sequencing and editorial type; a dashboard's signature element might be a particularly clear information hierarchy rather than any decoration at all. **Do not reuse the same signature move across unrelated projects** — if the last three sites all got a diagonal-cut hero or a bento grid, that's a sign to design the next one from this project's own identity instead.

This brief is what later QA stages (critique, audit) check the build against — it is the reference for "does this feel intentional," not a formality to skip.
