# Review, QA, and the Five-Stage Refinement Pass

## Visual verification (mandatory whenever browser/screenshot tools are available)

Don't consider a build finished because the code compiled. Run:

**Build → Render → Inspect → Critique → Correct → Render again → Verify**

### Viewports

320, 375, 390, 768, 1024, 1280, 1440px, at minimum.

### Check at each

- Horizontal overflow (scrollWidth vs. clientWidth should match except for intentional horizontal-scroll components)
- Clipped or truncated text
- Overlapping elements
- Mobile navigation actually works (opens, closes, traps focus correctly, closes on Escape/outside click)
- Touch target sizing
- Image cropping/subject framing
- Typography hierarchy still reads correctly at each size
- Spacing rhythm and alignment
- Contrast
- Focus visibility
- Keyboard navigation through the whole page/flow
- Interaction behavior (clicks, hovers, drags all do what they should)
- Animation smoothness (watch for dropped frames, especially on scroll-linked motion)
- `prefers-reduced-motion` actually produces the gentler variant
- Error and loading states, deliberately triggered
- Browser console: zero unexpected errors

**Verify real user journeys, not just static screenshots** — walk through the actual task (submit the form, complete the checkout, find the article) at more than one viewport.

### Honesty discipline

If no browser/testing tool is available in the environment: say so plainly, give specific manual-testing instructions, and clearly mark what hasn't been verified. **Never claim to have inspected a screenshot, run a test, or measured a performance number that didn't actually happen.** This applies to every section above and to [performance-and-seo.md](performance-and-seo.md)'s Core Web Vitals.

### Targets

WCAG 2.2 AA where applicable; Core Web Vitals (LCP/INP/CLS) as meaningful, honestly-reported targets.

---

## The five-stage refinement pass (from Impeccable)

Run this explicitly — as an actual pass over the work, not a rhetorical label — before calling a build done.

### 1. Craft
**Input**: the brief and the design direction from [design-direction.md](design-direction.md). **Action**: establish concept, IA, visual hierarchy, and an implementation plan. **Output**: a build worth critiquing. **Acceptance**: the plan maps cleanly onto the brief's mode, dials, and signature element.

### 2. Critique
**Input**: the built surface. **Action**: review it as a working creative director would — identify weak differentiation, inconsistent hierarchy, repetitive composition, decoration with no function, unclear communication. **Output**: a specific list of what's underperforming and why. **Acceptance**: every critique point names a concrete fix, not just a vague "feels off."

### 3. Audit
**Input**: the critiqued build. **Action**: evaluate functionality, accessibility, responsiveness, performance, and technical implementation against [accessibility-and-usability.md](accessibility-and-usability.md), [frontend-engineering.md](frontend-engineering.md), and [performance-and-seo.md](performance-and-seo.md). **Output**: a findings list by severity (see below). **Acceptance**: no unresolved critical finding remains.

### 4. Polish
**Input**: the audited build. **Action**: refine motion timing, component spacing, type rendering, hover/press behavior, transitions, alignment, image treatment, micro-interactions, focus/active states — the details that separate "working" from "considered." **Output**: the near-final build. **Acceptance**: nothing in the mandatory quality gates (SKILL.md) is still failing.

### 5. Distill
**Input**: the polished build. **Action**: remove anything that doesn't earn its place — unused complexity, decoration with no function, animation that doesn't pass the motion decision framework, copy that doesn't add information. **Output**: the shipped build. **Acceptance**: removing anything further would cost real information or usability, not just visual noise. **Distinguish refinement from redesign** here — a distill pass should not quietly replace the project's established identity; if the instinct is to redesign rather than trim, name that explicitly and confirm before doing it.

## Reporting findings

Report findings by **severity, evidence, impact, and recommended correction** — not a bare list of complaints:

- **Critical** — broken functionality, a real accessibility blocker, a security/privacy issue, or a content-authenticity violation. Ships regardless of visual score; fix before anything else.
- **Major** — a clear usability or craft problem a user would notice and be bothered by.
- **Minor** — a polish-level issue that would improve the result but doesn't block shipping.

A high visual/design score never excuses an unresolved critical finding — see [evaluations/quality-rubric.md](../evaluations/quality-rubric.md).
