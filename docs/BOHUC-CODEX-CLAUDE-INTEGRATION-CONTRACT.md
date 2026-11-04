# BOHUC — Codex / Claude Code Integration Contract

**v1.0 | 2026-11-04 | Demo only | Owner-approved collaboration scope**

## Objective and baseline
Redesign the **existing** BOHUC public website to premium quality while preserving the **existing** backend, Admin CMS, data models, media, publishing, SEO and enquiry workflows. **Codex owns backend/CMS and integration verification; Claude Code owns frontend visual design and implementation.**

Verified *local* baseline: commit `6617cfc9384bba6f950b7d8d247cfb2350e6e470`, tree `21fcfdb3a5f90f06f6033d2fe03df62a4a301c3f`, version `3.0.1`, `1,534/1,534` local tests passed. Formal acceptance remains **104/112**. Deferred R2 recovery/Preview gates are **DEMO-WAIVED, not PASSED**. No Cloudflare, spend, remote deploy, Git push or merge is authorized here.

**Critical:** GitHub `main` may not contain the frozen local commit. Both agents MUST verify the exact local Git object and available worktrees before acting. If unavailable, STOP; do not substitute an older remote tree, reset, clean or alter frozen/canonical dirty worktrees, historical audit material or read-only build artifacts.

## Ownership / limits

| Surface | Codex | Claude Code |
|---|---|---|
| CMS/Admin, D1/R2, migrations, API handlers, authentication, media lifecycle, publication, lead inbox, Workers/config | **Owner**: preserve and verify; changes only with owner approval | Read interfaces only; no writes |
| Public site visual system, typography, layout, presentational components, CSS, motion, responsive interactions | Verify contracts, accessibility and functionality; do not impose stylistic taste | **Owner**: redesign and implement |
| Public routes, form destinations, project content bindings, draft/publish isolation, canonical/OG/robots, error handling | Contract custodian and reviewer | Preserve; request changes explicitly |
| QA and integration | **Owner**: diff review, targeted tests and final full suite | Browser screenshot critique, visual tests and fixes |
| Budget, deployment, release branch merge/push, provider access | Ask owner first | Ask owner first |

**File ownership is not a glob.** The public `src/**` can include both presentation and protected logic. Codex must produce a specific frontend-editable file list from the candidate; anything not included is protected. Protect `admin/**`, `packages/**`, migrations, backend handlers, API/auth, lead/media/publication code, shared contracts, infra, and release files by default. Mixed-responsibility files require owner-approved cross-agent change requests. Claude must not replace the framework or introduce a second CMS to achieve a visual goal.

## Source/worktrees and communication

1. Codex verifies the local baseline and sets up **separate isolated local Git worktrees** for Claude implementation and Codex review. Suggested design branch: `design/bohuc-claude-frontend`. Never allow concurrent edits to the same files/worktree.
2. This Markdown file is the **shared policy**, not a live message bus. Both agents must be instructed to read it; existence in GitHub does not automatically load or notify either agent.
3. Keep operational handoffs in a small `agent-handoff/` directory associated with the isolated design workspace, **outside frozen release artifacts**. Keep one short current status note; no new audit bureaucracy.
4. **Codex → Claude START:** produce `agent-handoff/BACKEND-CONTRACT.md` from actual code: base SHA; precise editable/protected files; routes; CMS public data model and interface locations; project/media/layer data; publishing and SEO; forms/auth boundaries; local fixture commands and tests. Cite repository paths for claims and mark unverified APIs UNKNOWN. Claude acknowledges these boundaries.
5. **Claude → Codex DESIGN:** produce `agent-handoff/DESIGN-BRIEF.md`: honest critique of current site; BOHUC-specific visual direction and signature interaction; desktop/mobile layouts; accessibility, motion and reduced-motion strategy; exact expected files/assets/dependencies. Then implement within approved edit list. Design the existing website, not a substitute prototype.
6. **Contract changes:** if Claude needs new fields, different API shapes, route/SEO changes or protected-file edits, submit `agent-handoff/CHANGE-REQUEST.md` with need, current contract, minimal alternative, risk, files. Codex reviews; **owner must authorize** before either agent changes protected behavior. Otherwise Claude adapts to existing CMS.
7. **Claude → Codex HANDOFF:** produce `agent-handoff/CLAUDE-HANDOFF.md` with base/head SHA, changed paths, rationale, build outcome, screenshot locations at multiple widths, interactions/keyboard/reduced-motion results, asset licenses and known defects. Provide reproducible **running local preview**, not only screenshots.
8. **Codex → Claude REVIEW:** produce `agent-handoff/CODEX-REVIEW.md` with `APPROVED / CHANGES REQUESTED / BLOCKED` and reproducible findings for contract regressions. Claude fixes frontend issues in its worktree. Codex handles backend proposals only if owner-approved; do not silently undo Claude's design.
9. **Owner reviews final site** before authorizing merge, push or any external action.

Message header for each handoff:
```text
FROM / TO:
BASE SHA / HEAD SHA:
WORKTREE:
FILES CHANGED:
PROTECTED CONTRACT IMPACT: NONE | details
TESTS + SCREENSHOTS:
DECISION REQUESTED:
BLOCKERS:
NEXT AUTHORIZED ACTION:
```

## Protected product behavior

- Public content comes from the existing published CMS presentation model, never invented hard-coded project data or a parallel backend.
- D1 draft/publish isolation, READY R2 media and gallery ordering, five construction layers (visibility, alt/focal controls), project detail rendering, and public fallback/fail-closed behavior must survive.
- Admin editing, publishing, errors, SEO settings and lead inbox remain intact; no Admin redesign is part of this task.
- Preserve routes, primary navigation destinations, enquiry submission, SEO canonical/OG/robots/sitemap and working forms. Do not invent customer projects, awards, credentials or business facts.
- Ensure semantic HTML, keyboard/focus access, safe errors/loading, no overlapping/clipped text or horizontal overflow at `320, 375, 390, 768, 1024, 1280, 1440px`, `prefers-reduced-motion`, and sensible performance/asset licensing.

## Verification and release gates

**Baseline:** don't rerun the completed 1,534 tests on unchanged baseline merely to regenerate evidence.

**Claude:** inspect the current site, implement real frontend changes, run local preview, capture before/after screenshots, critique and fix real defects.

**Codex:** independently review the exact changed candidate, protected-file diff, CMS-powered page, five layers/media, published vs draft, forms/SEO, Admin smoke test, responsiveness, and browser console/accessibility. Run targeted tests during changes; on the **final integrated candidate**, run `npm run verify:all` once in a Windows environment allowing `127.0.0.1` plus Admin build. Preserve exact results; don't disable assertions.

This is an isolated **local demo**. It is **not** a production release, does not make the acceptance score 112/112, and grants **no** R2 inventory/downloads, D1 export, Cloudflare requests, live deployment, scheduler activation, billing changes, new credentials or remote Git publication. Obtain owner approval separately for any of these.

## Agent entry instructions

**Codex:** read this contract; verify frozen local SHA; derive precise contract/file-level ownership from existing code; set up safe isolated design worktree; prepare BACKEND-CONTRACT.md; check supported Claude Code CLI availability; hand off and STOP for Claude.

**Claude Code:** read this contract, BACKEND-CONTRACT.md and the `premium-frontend-director` skill; inspect real existing pages and CMS bindings; produce DESIGN-BRIEF.md and implement the redesign in the isolated worktree; hand off running preview and CLAUDE-HANDOFF.md to Codex. Do not change backend.

## Related source material
- `ThisismynameNOT/Claude/.claude/skills/premium-frontend-director/SKILL.md` and mirrored `.agents/skills/premium-frontend-director/` (different installation paths, one shared skill).
- `workflows/redesign.md`, `references/frontend-engineering.md`, `references/github-repository-research.md`, `references/review-and-audit.md`.
- `ThisismynameNOT/BOHUC-Improved` README for architecture discovery **only**; the pinned **local** commit is authoritative.

**Definition of done:** an attractive, genuinely functional local BOHUC redesign driven by its existing CMS, with independent Codex integration PASS and owner visual acceptance. Not production deployment or automatic 112/112.
