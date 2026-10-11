# Frontend Engineering

Design quality and engineering quality are one deliverable. A beautiful interface that doesn't work, doesn't ship clean, or breaks existing functionality has failed regardless of how it looks.

## Stack

Support the environment that's actually in play rather than forcing one: plain HTML/CSS/JS, React, Next.js, Vue, Svelte, Astro, Tailwind, an existing design system, or a CMS-driven setup are all valid targets. **Honor the existing project's architecture.** Don't swap frameworks, add a major new dependency, or introduce a competing styling approach without a clear, stated reason — "I'd prefer X" is not sufficient justification when a project already has a working Y.

## Production-grade baseline

- **Semantic HTML** and accessible interaction patterns (see [accessibility-and-usability.md](accessibility-and-usability.md)).
- **Responsive behavior** verified at real breakpoints, not assumed from a single viewport.
- **Maintainable component structure** — reusable components for repeated patterns, sensible prop/variant APIs, no copy-pasted near-duplicate blocks.
- **Sensible design tokens** — colors, spacing, type scale, radii defined once and referenced, not hard-coded per component.
- **Safe dependency usage** — don't add a library for something a few lines of native code covers; pin versions sensibly; avoid abandoned/unmaintained packages for anything load-bearing.
- **Proper asset loading and image optimization** — appropriately sized/formatted images (modern formats where supported, with fallback), lazy-loading below the fold, explicit dimensions to prevent layout shift.
- **Layout stability** — reserve space for images, embeds, and async content so nothing jumps after load (this is also a Core Web Vitals requirement — see [performance-and-seo.md](performance-and-seo.md)).
- **Functional navigation and forms** — links go where they say, forms actually submit/validate/handle errors, nothing is a styled dead end.
- **Correct error handling** — network failures, empty states, and invalid input all have a defined, user-visible behavior, not a silent failure or a raw stack trace.
- **Consistent interactive states** — hover, focus, active, disabled, loading defined for every interactive element, not just the default state.
- **Clean console output** — no errors, and no debug `console.log` noise left in shipped code.
- **Cross-browser compatibility** — verify in at least two engines when the environment allows it (e.g., Chromium + WebKit/Safari); flag anything untested.

## Protecting existing projects

When working on an existing site/app (redesign or refine), treat the following as protected unless the user explicitly asks to change them:

- Routes and URL structure
- Navigation behavior and labels
- Form field names, order, and integrations (renaming breaks analytics and autofill)
- CMS schemas and existing content
- Analytics/tracking event names
- Existing APIs and auth flows
- Accessibility behavior already working (don't regress a working focus trap or alt-text pattern while "improving" the visuals)
- Critical business workflows (checkout, booking, signup) — these get extra caution and, ideally, a before/after walk-through of the flow, not just the individual screens

**Never silently alter backend behavior to accommodate an aesthetic decision.** If a visual idea requires a data/API shape change, say so explicitly and get confirmation rather than quietly expanding scope.

## SEO fundamentals (for public-facing sites)

- Descriptive, accurate `<title>` and meta description per page.
- One logical heading structure per page (see accessibility section).
- Semantic markup search engines can parse (not everything as generic `<div>`s).
- Open Graph / Twitter Card metadata for social sharing where the page will plausibly be shared.
- Structured data (JSON-LD) where it genuinely applies (local business, article, product) — don't add schema that doesn't match the actual content.
- A working `sitemap.xml` / `robots.txt` for multi-page sites where the platform doesn't generate one automatically.
