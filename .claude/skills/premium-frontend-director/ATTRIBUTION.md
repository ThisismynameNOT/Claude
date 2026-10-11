# Attribution

This Skill is a synthesis and extension, not a reproduction, of three independent public design/engineering resources. No file in this Skill is a copy of any upstream file; concepts, named rules, and canonical technical values (easing curves, dial definitions, workflow stage names) are restated in original wording and reorganized into a different structure, with new material added throughout (the priority hierarchy, the art-direction-first workflow, content-authenticity gating, the quality rubric, and the examples/evaluations directories have no direct upstream equivalent).

## Sources

### Emil Kowalski's design/animation skills
Repository: `emilkowalski/skills` — https://github.com/emilkowalski/skills
Contribution to this Skill: the motion decision framework (should-it-animate gate, purpose-naming, tool selection), canonical easing curves and duration tables, spring configuration guidance, transform/opacity-only discipline, transform-origin-at-trigger convention, and interruption/exit handling. Used primarily in [references/motion-and-interactions.md](references/motion-and-interactions.md) and [workflows/animate.md](workflows/animate.md).

### Impeccable
Repository: `pbakaus/impeccable` by Paul Bakaus — https://github.com/pbakaus/impeccable
License: Apache License 2.0.
Contribution to this Skill: the craft → critique → audit → polish → distill five-stage refinement structure, the four-mode framing (Persuade/Operate/Read/Experience), and the refinement-vs-redesign distinction. Used primarily in [references/review-and-audit.md](references/review-and-audit.md), [references/design-direction.md](references/design-direction.md), and the `workflows/` directory's mode-aware structure. No Impeccable source code, scripts, or binary tooling is included or required by this Skill — this Skill's workflows are self-contained markdown instructions, not a wrapper around the Impeccable CLI/engine.

### Taste-skill
Repository: `Leonxlnx/taste-skill` by Leonxlnx — https://github.com/Leonxlnx/taste-skill
Contribution to this Skill: the anti-"AI slop" default-avoidance checklist (typography/color/layout tells, generic-content tells), the three-dial system (`DESIGN_VARIANCE`/`MOTION_INTENSITY`/`VISUAL_DENSITY`), and the redesign preservation protocol. Used primarily in [references/typography-and-color.md](references/typography-and-color.md), [references/layout-and-responsive.md](references/layout-and-responsive.md), [references/content-and-brand-authenticity.md](references/content-and-brand-authenticity.md), and [references/design-direction.md](references/design-direction.md).

**Material change from the source**: Taste-skill's defaults (e.g., the em-dash ban, the Inter/Fraunces font avoidance, the 3-column-card avoidance) are treated in this Skill as **defaults to avoid, not absolute prohibitions** — subordinate to the user's explicit requirements per the priority hierarchy in [SKILL.md](SKILL.md). This is a deliberate, documented divergence; see [CHANGELOG.md](CHANGELOG.md).

## License note

No upstream license text, substantial verbatim passages, or proprietary tooling (Impeccable's compiled binaries, CLI, or paid catalog service) are redistributed here. If any upstream project's license requires attribution for derived guidance of this kind, this file is that attribution. This Skill itself is provided for the requesting user's own use; no license is asserted over the three upstream projects beyond what their own repositories already grant.
