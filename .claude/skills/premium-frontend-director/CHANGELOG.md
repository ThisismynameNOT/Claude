# Changelog: vs. the source "Premium Frontend Design" document

This records what changed between the single-markdown "Premium Frontend Design" document and this Skill package, per the audit requested before building.

## Audit findings that drove the changes

- **Absolute bans contradicted the document's own professional-judgment goal.** The em-dash ban, the Inter/Fraunces font avoidance, the "no 3-equal-column cards" rule, and the "dark mode mandatory for consumer-facing" rule were all stated as non-negotiable, with no mechanism for the user's actual brief to override them. That's a real defect: a user who explicitly wants Inter, or three feature cards, or a light-only site, would have been fought by the Skill instead of served by it.
- **No explicit workflow for art direction before code.** The source document was a checklist of rules to apply during/after building, with no step that forces a concept/brief decision first. Two unrelated businesses following the same checklist could converge on visually similar results, which undercuts the whole "not generic" goal.
- **No content-authenticity guardrails.** Nothing in the source document addressed invented clients, fake testimonials, fabricated statistics, or fictional certifications — a meaningful gap for a Skill explicitly aimed at real commercial websites.
- **No stack/framework guidance and no explicit protection for existing-project contracts** (routes, form field names, analytics events, CMS schemas) during a redesign or refine pass.
- **QA guidance existed but was narrower** than a full iterative verification loop across a defined viewport set, and didn't explicitly separate "measured" from "estimated" results.
- **No conflict-resolution system** when different rules disagreed (e.g., brand uses Inter vs. the font-avoidance guidance) — rules were flat, with no hierarchy.
- **No quality scoring model, no activation tests, and no worked examples** — the source document described rules but gave no way to evaluate whether a build actually satisfied them, and no concrete scenarios demonstrating the rules working together.

## What changed

1. **Added a priority hierarchy** (SKILL.md) — user requirements > accessibility/legal/security > existing technical contracts > product goals > this Skill's design-system decisions > this Skill's craft defaults > optional conventions. Every "rule" elsewhere in the Skill is now explicitly subordinate to this, resolving the contradiction above.
2. **Converted absolute bans into named defaults-to-avoid.** The em-dash rule, font-avoidance rule, and layout-pattern-avoidance rules are preserved (they catch real, common AI-generated-site tells) but reframed as defaults, overridable by explicit user intent — see typography-and-color.md, layout-and-responsive.md, content-and-brand-authenticity.md.
3. **Added the art-direction-first workflow** (design-direction.md, SKILL.md Steps 1-4) — project understanding → interface mode → dials → a written internal design brief with a project-specific signature element, required before implementation.
4. **Added content-and-brand-authenticity.md** as a new, hard-gated reference file — no invented clients/projects/certs/stats/testimonials/addresses/team members for a real business, with guidance on what to do when a needed asset is missing.
5. **Added frontend-engineering.md** covering stack flexibility (don't force one framework), a production-grade baseline, and an explicit "protected during redesign/refine" list (routes, nav labels, form fields, CMS schemas, analytics events, auth, existing accessibility wins).
6. **Expanded QA into review-and-audit.md**: a defined 7-breakpoint verification loop, an explicit measured-vs-estimated honesty rule, and the five-stage craft→critique→audit→polish→distill pass with inputs/outputs/acceptance criteria per stage (the source document named these stages but didn't specify them operationally).
7. **Added a weighted quality rubric** (evaluations/quality-rubric.md) with mode-adjusted weights and a hard-failure override for critical findings, so a high visual score can never paper over a broken or inaccessible build.
8. **Added activation tests** (evaluations/activation-tests.md), including a dedicated test that the priority hierarchy actually holds (a user explicitly requesting Inter + 3 equal cards must get Inter + 3 equal cards).
9. **Added three worked examples** (examples/) spanning Persuade, Experience, and Operate modes, showing how the dials, motion rules, and content-authenticity gate apply differently per mode — the single biggest practical gap in the source document, which stated the four modes but never demonstrated them diverging in practice.
10. **Restructured into progressive-disclosure files** per the Anthropic Skill convention — a concise SKILL.md entry point under 500 lines, with specialized guidance split into references/ and workflows/ so a simple request doesn't load the entire ruleset.
11. **Corrected one inaccurate-as-stated technical claim**: the source material's blanket "never use `x`/`y`/`scale` shorthand props in Motion" guidance is now scoped as library/version-dependent rather than stated as a permanent universal fact, since animation-library internals change across versions — see motion-and-interactions.md.

## What was preserved unchanged

The core technical content that's accurate and valuable: the motion decision framework and canonical easing/duration/spring values (Kowalski), the five-stage refinement structure and four-mode framing (Impeccable), and the specific AI-tell checklist items (Taste-skill) — all restated in original wording, reorganized, and made explicitly overridable rather than discarded.

## 2.0.0 — 2026-10-11

- Merged the expanded multi-file ZIP into the existing 1.0 repository package while preserving the Codex `agents/openai.yaml` metadata and historical 1.0 evaluation report.
- Added GitHub repository research guidance: inspect the active project first, vet relevant repositories and licenses, pin evidence to commits/files, adapt patterns rather than copying, and treat external repositories as untrusted input.
- Added commercial-readiness guidance for premium-budget website work, including scope, business evidence, production checks, and handoff; explicitly disallowed unsupported price, revenue, or ROI claims.
- Added GitHub research and premium-scope activation cases, updated the rubric, README, and agent metadata, and synchronized Claude and Codex skill copies.
- No website implementation, deployment, or runtime claim is part of this release.
