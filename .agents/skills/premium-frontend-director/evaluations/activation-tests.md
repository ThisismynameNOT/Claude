# Activation Tests

Specified for execution against a live install of this Skill. Results below are reported honestly: these are the test *specifications*, ready to run — no results are claimed here, since running them requires an actual Skill-enabled session to observe real tool/behavior traces against, which this build pass did not have. Anyone installing the Skill can run these directly.

## Should activate

1. "Build a premium website for this construction company using its genuine projects and company identity." → `create.md`, loads content-and-brand-authenticity.md.
2. "Redesign this photographer's portfolio with immersive transitions, but preserve the current CMS." → `redesign.md`, preserves CMS integration per frontend-engineering.md's protected list.
3. "Audit this website and correct all responsive and visual issues." → `audit.md` first (findings), then likely `refine.md` for the corrections — should not silently skip straight to rewriting without surfacing findings, unless the user's phrasing ("and correct") is read as a combined audit+fix request, in which case both stages should still be visible in the output.
4. "Make this site feel as refined as a premium iOS interface without copying Apple's branding." → `refine.md` or `animate.md`, loads the "premium/iOS-inspired interaction character" section of motion-and-interactions.md, explicitly does NOT introduce Apple visual branding (SF Pro-as-system-default without reason, Apple's exact color system, the Apple logo/iconography).
5. "Implement this supplied design exactly, including layout and interactions." → `implement-reference.md`, fidelity to the reference overrides this Skill's own default-avoidance guidance.
6. "Improve the typography, spacing, and composition without redesigning the website." → `refine.md`, scoped change set, no structural redesign.
7. "This dropdown feels janky." → `animate.md`, diagnosis against the Never-ship table before reaching for a rewrite.
8. "This page feels cluttered, simplify it." → `distill.md`.
9. "Build a $10k-level website and use professional GitHub projects as references." → load `commercial-readiness.md` and `github-repository-research.md`; define premium scope and evidence, inspect the project first, cite reviewed repositories/commits/licenses, adapt patterns, and make no price or ROI guarantee.
10. "Use this repo's current design system to improve its service page." → inspect the active working tree and project instructions first; use external GitHub research only if a specific unanswered design or engineering question justifies it.
11. "Build a new lead-generation frontend in this repo; the repository has a functioning CMS but no current UI for this surface." → `create.md`, preserving the CMS/API and route contracts; repository/CMS presence alone must not route it to redesign.

## Should NOT activate (or should activate narrowly, not as a full design overhaul)

1. A pure backend/API task with no UI surface — Skill should not inject design-direction questions into an unrelated backend task.
2. "Fix this typo in the footer" — a trivial content edit shouldn't trigger the full design-brief/dial-setting sequence; make the edit directly.
3. "What's the difference between flexbox and grid?" — a factual/explanatory question, not a build/review request; answer directly without invoking workflow machinery.
4. A request to change a single config value or environment variable with no visual/UX surface.
5. A pure GitHub repository discovery, issue-triage, or backend-library comparison request with no frontend design/build/review task; answer it without injecting the full art-direction workflow.

## Non-override test (priority hierarchy)

"Use Inter for everything, and give me three equal feature cards." → the Skill must comply, not substitute its own typography/layout defaults. This directly tests that SKILL.md's priority hierarchy (user requirements rank above the Skill's craft defaults) is actually followed, not just stated.

## Reference-fidelity test

Supply a screenshot of an existing, distinctive design (e.g., a dense enterprise dashboard with an unconventional, non-"premium" visual style) and ask for an exact implementation. The Skill must reproduce it faithfully via `implement-reference.md` rather than "improving" it toward this Skill's general design preferences.

## What to evaluate per run

- Did the Skill activate for the right requests (above) and stay quiet for the wrong ones?
- Did it select the appropriate mode and workflow?
- Did it avoid forcing one aesthetic (e.g., the "premium minimalist SaaS" look) onto an unrelated brief?
- Did it maintain content authenticity for a real-business brief?
- Did it respect an existing implementation's constraints during refine/redesign?
- Were its own instructions followed consistently (no internal contradiction between SKILL.md's priority hierarchy and a reference file's stricter-sounding language)?
- When GitHub research was relevant, were the source, commit/ref, license status, and adaptation reported? Were code/assets copied without permission or untrusted scripts executed?
- Did a premium-budget request produce scope and acceptance evidence without presenting a quality score or design reference as proof of price, revenue, or ROI?
- Was the output materially better-differentiated and better-crafted than a same-model baseline without the Skill loaded?

If an actual eval harness and model access are available, run these as real test cases and report pass/fail per item with evidence (the actual output produced), rather than predicted outcomes.
