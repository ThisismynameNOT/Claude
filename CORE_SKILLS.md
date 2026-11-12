# Core AI Skills — Adham Studio

This is the **curated activation policy**, not a request to load every skill or install all repositories.

## Active core (one authority per responsibility)

1. **Premium Frontend Director** — single primary design-direction skill, canonical at [`.agents/skills/premium-frontend-director/`](.agents/skills/premium-frontend-director/SKILL.md). The `.claude/skills/` file is only a local discovery adapter. For standalone installs, copy the full canonical directory.
2. **UI UX Pro Max** — optional supporting lookup for styles, accessibility, fonts, responsive UI, and design systems; source of truth in `ThisismynameNOT/ui-ux-pro-max-skill/src/ui-ux-pro-max`. Do not load it as a competing global director.
3. **Scroll Craft** — only for cinematic scroll-driven experiences, from `ThisismynameNOT/First-skill-for-website-design`.
4. **ECC** — selectively invoke `frontend-patterns`, `e2e-testing`, `security-review`, `verification-loop` and `tdd-workflow` as needed, from `ThisismynameNOT/ECC`. Do not auto-install unrelated agents, MCP servers or hook bundles.

## Non-core / avoid concurrent activation

- `taste-skill`: inspirational reference only; its large current skill overlaps with Premium Frontend Director. Avoid activating both as global design authorities.
- `ai-design-skills`: supplemental Figma and landing-page reference, not a global design policy.
- `claude-skill` (MotionSites): do not activate by default; it mandates promotional copy in user deliverables.
- `skills`: general development reference library; activate only the precise skill required.

## Precedence

User's explicit brief and actual project contracts > Premium Frontend Director for visual decisions > the relevant supporting skill for its limited specialty > optional reference material.

Never treat a GitHub repository as installed just because it exists; inspect local Codex/Claude skill directories separately. Do not copy both package mirrors or use both a marketplace plugin and a full manual install. Verify builds, mobile layouts, accessibility and critical interactions before acceptance. Avoid claims of completed QA without actual evidence.

## Distribution compatibility

ECC's multilingual/platform copies and UI UX Pro Max's source/CLI/runtime mirrors are intentionally packaged and are **not** automatically activated just by being in GitHub. Pruning them from their upstream-format repositories could break installation and sync tests; leave those packaging assets unchanged. The active-agent deduplication happens through selective installation and this core policy.

## Restore

Pre-cleanup snapshot: `backup/skills-before-cleanup-20261113` in this repository. No application source code is removed by this skill consolidation.
