# Premium Frontend Director

A portable Agent Skill for creating, redesigning, refining, animating, implementing from references, and auditing websites and web application interfaces. This release combines the earlier repo version with the fuller multi-file package and adds project-aware GitHub research plus commercial-readiness guidance.

## Install

The GitHub repository keeps matching copies in both supported locations:

- **Codex:** `.agents/skills/premium-frontend-director/` — invoke with `$premium-frontend-director` or select it from `/skills`.
- **Claude Code:** `.claude/skills/premium-frontend-director/` — invoke with `/premium-frontend-director` or let Claude Code select it when the task matches.
- **Other Agent Skills-compatible tools:** install the folder in the documented skills directory for that tool. Discovery paths vary.

Keep the full directory structure so the skill can load its workflows, examples, evaluations, and references. If you edit the skill, update both GitHub copies together.

## Use

Give it a concrete task, such as:

- “Create a Czech construction website using the real company information and project photos I provide. Inspect our existing GitHub project first.”
- “Refine the pricing page layout but keep the current design system and checkout behavior.”
- “Audit the dashboard for keyboard, responsive, and interaction defects.”
- “Implement this supplied screenshot closely and report any visual differences you could not verify.”

For existing projects, it examines the active code and project contracts first. When useful, it researches relevant GitHub repositories, checks source and maintenance evidence, and reports how a pattern was adapted. It does not copy another company's identity or code, invent real-business facts, or claim that a website is worth a specific fee. “$10k+ quality” is treated as a quality and scope target, not a financial guarantee.

The skill selects one of seven workflows: create, redesign, refine, animate, audit, implement-reference, or distill. It loads supporting guidance as needed and reports verification limits honestly.

## Package contents

- `SKILL.md`: activation and workflow router.
- `agents/openai.yaml`: Codex display and invocation metadata.
- `workflows/`: task procedures.
- `references/`: design, engineering, GitHub research, commercial scope, and QA guidance.
- `examples/`: worked website and application scenarios.
- `evaluations/`: activation scenarios and quality rubric.
- `EVALUATION_REPORT.md`: checks actually performed for this release.
- `EVALUATION_REPORT_1.0.md`: preserved report for the previous package.
- `ATTRIBUTION.md`: conceptual sources and license notes.
- `CHANGELOG.md`: release history.

## License

No license is declared for this package. Upstream projects listed in `ATTRIBUTION.md` retain their own licenses. Set a package license before redistributing it under an open-source license.
