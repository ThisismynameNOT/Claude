# Premium Frontend Director

A portable Agent Skill for creating, redesigning, refining, animating, implementing from references, and auditing websites and web application interfaces.

## Install

### Claude.ai

Upload `premium-frontend-director.zip` from **Customize → Skills → Create skill → Upload a skill**. Enable it in your skills list. Claude's account and organization settings may control whether custom skills are available.

### Claude Code

For one repository, place this folder at `.claude/skills/premium-frontend-director/`. For personal use across local projects, place it at `~/.claude/skills/premium-frontend-director/`. Start a new session or invoke the skill by name.

### Other Agent Skills compatible tools

Install the folder in the tool's documented skills directory. The package uses standard `SKILL.md` YAML frontmatter and linked Markdown resources; exact discovery paths vary by tool.

## Use

Ask for a concrete task, for example:

- “Create a Czech construction website using the real company information and project photos I provide.”
- “Refine the pricing page layout but keep the current design system and checkout behavior.”
- “Audit the dashboard for keyboard, responsive, and interaction defects.”
- “Implement this supplied screenshot closely and report any visual differences you could not verify.”

The skill selects a workflow from the request and loads only the references needed for it. It does not install frameworks, invent company facts, or claim tests that were not run.

## Package contents

- `SKILL.md`: short activation and workflow router.
- `references/`: reusable design, engineering, and QA guidance.
- `workflows/`: task procedures with inputs, outputs, and acceptance criteria.
- `examples/`: Czech construction, photography, and dashboard scenarios.
- `evaluations/`: activation scenarios and evidence-based scoring rubric.
- `EVALUATION_REPORT.md`: checks actually performed for this release.
- `ATTRIBUTION.md`: conceptual sources and license notes.
- `CHANGELOG.md`: changes from the supplied specification.

## License

No license is declared for this new package. The upstream projects listed in `ATTRIBUTION.md` retain their own licenses. Set a package license before redistributing it under an open-source license.
