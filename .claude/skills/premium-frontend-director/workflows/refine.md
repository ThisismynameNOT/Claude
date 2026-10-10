# Refine an existing interface

## Inputs

Use the user's narrow objective and current page/component as the source of truth.

## Procedure

1. Inspect the component and relevant surrounding system, styles, data, and interaction behavior.
2. State the change boundary internally: what changes and what must remain unchanged.
3. Identify the smallest edit that solves the observed problem. Keep current brand, copy, navigation, routes, functionality, and component contracts outside scope.
4. Make the edit using existing tokens and patterns. Do not opportunistically rewrite unrelated components.
5. Check the exact affected state and one adjacent regression surface. Run the relevant test or build if the change touches behavior.

## Deliver

Report the focused change, preserved behavior, checks actually performed, and any unverified state.

## Acceptance

- The requested issue is fixed with no unrequested design-system change.
- Adjacent behavior and focus/keyboard affordances still work.
- The result is visually checked at the affected responsive state when tools are available.
