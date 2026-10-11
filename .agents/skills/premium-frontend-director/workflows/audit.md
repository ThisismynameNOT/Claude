# Workflow: Audit

**Activates when**: the request is a structured review — "audit this site," "check accessibility and responsiveness," "what's wrong with this page" — rather than a request to change anything yet.

## Steps

1. Scope the audit: visual/UX, technical (a11y/perf/responsive), content authenticity, or all of the above — infer from the request; default to all when unspecified.
2. Run the visual-verification loop from [references/review-and-audit.md](../references/review-and-audit.md) across the listed viewports if a browser/screenshot tool is available; otherwise say so and give manual-testing steps instead of guessing at results.
3. Evaluate against: [references/accessibility-and-usability.md](../references/accessibility-and-usability.md), [references/layout-and-responsive.md](../references/layout-and-responsive.md), [references/frontend-engineering.md](../references/frontend-engineering.md), [references/performance-and-seo.md](../references/performance-and-seo.md), and, for a real business, [references/content-and-brand-authenticity.md](../references/content-and-brand-authenticity.md).
4. Evaluate the critique lens too (differentiation, hierarchy, composition, communication clarity) from [references/review-and-audit.md](../references/review-and-audit.md) — a technical audit that ignores whether the design actually works is incomplete.
5. **Write the findings, don't just fix them**, unless the user asked for an audit-and-fix in one pass. Report by severity/evidence/impact/recommended correction, per [references/review-and-audit.md](../references/review-and-audit.md)'s reporting format.

## Severity definitions (reuse exactly)

- **Critical** — broken functionality, a real accessibility blocker, a security/privacy issue, a content-authenticity violation. Always reported regardless of how good the overall design is.
- **Major** — a usability or craft problem a user would notice and be bothered by.
- **Minor** — a polish-level issue, non-blocking.

## Acceptance criteria

- Every finding has evidence (what was actually observed, at what viewport/condition), not a generic claim.
- Findings are scored for severity and a high visual/design impression never suppresses a critical finding.
- What could and couldn't actually be tested in this environment is stated honestly — no fabricated measurements or unverified claims presented as fact.
- If the user wants fixes applied, hand off to [refine.md](refine.md) (scoped) or [redesign.md](redesign.md) (broad) as appropriate, rather than silently rewriting things mid-audit.
