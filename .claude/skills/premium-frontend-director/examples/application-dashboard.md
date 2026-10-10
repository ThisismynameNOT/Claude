# Example: professional SaaS dashboard

## Brief

Improve an operational dashboard where users scan status, filter records, and complete repeated tasks. Data accuracy, speed, and recovery matter more than decorative animation.

## Direction

Use **Operate** for workspace and task flows, **Read** for detailed reports. Tune `VISUAL_DENSITY` to actual user needs. Keep charts, tables, and controls easy to scan; do not inherit marketing-page motion.

## Implementation cues

- Preserve permissions, filters, saved state, APIs, and analytics events.
- Make loading, empty, partial, error, and success states explicit.
- Prefer native controls or established accessible widgets; define keyboard behavior for custom grids, menus, and tabs.
- Keep repeated actions immediate and easy to interrupt. Use feedback that does not displace the user's reading position.

## Acceptance evidence

Check a dense data state, no-results state, keyboard-only filtering, row/action behavior, error recovery, responsive overflow, focus visibility, and console output. Report performance only from actual measurements.
