# Audit a frontend

## Inputs

Use the target routes or codebase, expected journeys, audience, relevant devices, and explicit audit scope. Treat an audit as read-only unless the user also asks for fixes.

## Procedure

1. Identify the user-critical journeys and routes; inspect existing code and UI without changing state.
2. Review visual hierarchy, content accuracy, responsive layout, keyboard/focus, controls/forms, loading/empty/error states, console output, performance, SEO, and functional contracts as relevant.
3. Use browser or test tools when available. Capture exact route, viewport, state, reproduction steps, and tool output for each finding. Mark inferred or unverified conditions.
4. Classify findings by consequence and confidence using [review and audit](../references/review-and-audit.md). Do not report style preference as a defect without a user or product impact.
5. Provide prioritized corrections and the smallest verification that can confirm each correction.

## Deliver

Provide an executive summary and a finding list with severity, evidence, impact, confidence, and recommendation. Keep passed checks separate from checks not run.

## Acceptance

- Findings are reproducible or explicitly labeled as inferred.
- No hidden changes are made during a read-only audit.
- Critical risks are not averaged away by a score.
- No conformance or performance result is claimed without actual evidence.
