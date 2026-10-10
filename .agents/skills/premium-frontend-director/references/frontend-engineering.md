# Frontend engineering

## Work with the project

Inspect the existing framework, package scripts, components, tokens, routes, tests, and CMS contracts before editing. Follow local conventions. Support HTML/CSS/JavaScript, React, Next.js, Vue, Svelte, Astro, Tailwind, and other stacks without forcing a migration.

Do not replace or silently change:

- routes, URLs, navigation, or deep-link behavior;
- CMS schemas, slugs, content, or preview flows;
- forms, APIs, analytics events, or authentication;
- persistence, permissions, or business workflows;
- accessibility behavior or established design tokens.

Change these only when requested and preserve compatible behavior where possible.

## Implement deliberately

- Use semantic HTML and small, comprehensible components.
- Keep content separate from presentation where the project already does so.
- Reuse existing tokens and accessible primitives.
- Avoid unnecessary packages, abstractions, generated wrappers, and global CSS changes.
- Preserve loading, error, empty, success, and disabled states.
- Treat user data and URL input safely; do not weaken security to simplify styling.
- Keep links, buttons, forms, and menus functional, including keyboard use.

## Change management

For existing products, identify the functional contract before a redesign. Use focused edits where the user asks for refinement. Add or update meaningful tests for changed behavior when the project has a relevant test setup; do not create tests that merely restate a trivial styling edit.

## Verification

Run the project's relevant build, lint, type, or test commands when available. Inspect runtime errors and actual browser behavior when browser tools exist. Report exactly what ran, what passed, and what remains unverified. A successful compile does not prove accessibility, responsive quality, or workflow correctness.
