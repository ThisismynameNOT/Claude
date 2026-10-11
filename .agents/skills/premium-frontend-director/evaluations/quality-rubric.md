# Quality Rubric

A weighted, evidence-based scoring model for evaluating a build this Skill produced. Scores are assigned from what was actually observed (real inspection, real test runs) — never invented for a check that wasn't performed; an unperformed check is reported as "not evaluated," not scored.

## Weights (initial defaults — adjust per surface mode, see below)

| Category | Weight |
|---|---:|
| Art direction and originality | 20% |
| Usability and information architecture | 15% |
| Visual coherence and typography | 15% |
| Motion and interaction quality | 10% |
| Responsive implementation | 10% |
| Accessibility | 10% |
| Engineering quality and performance | 10% |
| Content authenticity and business effectiveness | 10% |

### Mode-based weight adjustment

These are starting weights for a Persuade surface. Adjust per mode:

- **Operate**: usability/IA and accessibility rise (to roughly 20-25% each); art direction/originality falls (to roughly 5-10%) — a dashboard is scored on whether it's fast and clear to use, not on how distinctive it looks.
- **Read**: visual coherence/typography rises; motion falls close to 0% — most Read surfaces should have little to no decorative motion.
- **Experience**: art direction/originality rises (to 25-30%); engineering/performance still matters fully (an immersive portfolio that's slow has failed regardless of its art direction).

State which weighting was used when reporting a score.

## Hard-failure override

**Critical findings (per [references/review-and-audit.md](../references/review-and-audit.md)) override the weighted score entirely.** A build with a 9/10 weighted score and one unresolved critical accessibility blocker, broken core functionality, or a content-authenticity violation is not a 9/10 build — report it as failing, with the critical finding named first, regardless of how the weighted categories score.

## Scoring discipline

- Score only what was actually evaluated. If accessibility wasn't actually tested (no screen-reader pass, no axe/Lighthouse run), say "not evaluated" for that category rather than guessing a plausible-sounding number.
- Separate hard, testable failures (a contrast ratio that measurably fails WCAG AA, a Lighthouse score that was actually run) from subjective design judgment (whether the hero composition is "distinctive enough") — label each finding as one or the other.
- A score is a communication tool, not a target to game. If a build scores well across every category but still feels generic, trust the qualitative read and say so — the rubric is a check on blind spots, not a replacement for judgment.

## Using this rubric

Apply it at the end of [workflows/audit.md](../workflows/audit.md) or as the final step of the five-stage refinement pass in [references/review-and-audit.md](../references/review-and-audit.md). Report scored categories with their evidence, "not evaluated" categories explicitly, and any critical override prominently at the top.

## Commercial-value boundary

This rubric evaluates observed implementation quality. It does not estimate a website's sale price, client willingness to pay, revenue, or ROI. For premium-budget work, use [commercial-readiness.md](../references/commercial-readiness.md) to review scope, business context, acceptance criteria, and handoff. Do not convert the weighted score into a dollar valuation.

## GitHub-evidence boundary

GitHub references can support decisions about implementation patterns, tests, and maintenance practices. They do not prove a design is professionally suitable for this brand. Cite the exact source and commit/ref, verify license status, and report how the pattern was adapted.
