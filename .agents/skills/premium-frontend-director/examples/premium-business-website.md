# Example: Czech Construction Company (Persuade mode)

Illustrates the workflow for a real commercial website — the case the Skill must handle without falling into a generic construction-company template.

## Brief (as a user might give it)

"Build a website for [real company], a Prague-based construction firm. Use their actual projects and contact info."

## How the Skill should work it

**Step 1 — Understand the project.** Don't invent what kind of construction firm this is — civil infrastructure, residential renovation, and industrial fabrication read completely differently. If the user hasn't said, check any supplied material (business registry listing, existing site, provided photos) before guessing, and state the assumption plainly if it's still a guess.

**Mode**: primarily Persuade (the site exists to generate leads), with a Read-mode project/case-study section if there's enough real material to support one.

**Dials**: a construction firm's credibility usually favors restraint — `DESIGN_VARIANCE` mid (4-6, enough asymmetry to avoid looking templated, not avant-garde), `MOTION_INTENSITY` low-mid (3-5, confidence reads as composed rather than flashy), `VISUAL_DENSITY` low-mid (generous section spacing, let real project photography breathe).

**Content authenticity (hard gate)**: use only the company's real projects, real contact details, real (or clearly placeholder-marked) team information. No invented certifications, no fabricated client logos, no made-up "20+ years" style claims unless the user actually stated it. If the business-registry phone number and a number mentioned elsewhere disagree, flag it rather than picking one.

**Signature element**: tied to this company's actual work — e.g., a materials/structure motif (steel, concrete, timber framing) expressed in the type/texture system, or a project-sequence visual (foundation → structure → finish) if their real projects support showing that. Not a generic "blueprint grid" applied regardless of what they actually build.

**Avoid the generic-template failure mode**: a near-identical hero + 3-card services row + testimonial carousel + contact form is the default a less-directed build reaches for. This Skill's layout defaults (zigzag cap, eyebrow restraint, default-away-from-3-equal-cards) exist specifically to push past that, while the priority hierarchy still lets the user override any of it explicitly.

## What "done" looks like

Real company data throughout, a visual system that would look wrong transplanted onto an unrelated industry, working contact/lead form, responsive at all required breakpoints, and a QA pass confirming no invented facts slipped in anywhere (copy, alt text, structured data).
