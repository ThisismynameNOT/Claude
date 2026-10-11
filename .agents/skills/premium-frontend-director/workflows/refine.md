# Workflow: Refine

**Activates when**: improving an existing interface — typography, spacing, composition, a specific component — without changing its established identity. "Improve the typography and spacing," "this feels a little off, tighten it up," "make this button feel better."

This is the narrowest-scope workflow. **Prefer targeted corrections to wholesale rewrites.** If the request could be satisfied by changing a handful of specific values (type scale, spacing tokens, a transition curve, a color's saturation), do that — don't regenerate the surrounding layout or introduce a new visual system as a side effect.

## Steps

1. Read the existing implementation directly — its actual tokens, component structure, and conventions — before proposing anything. The existing codebase is the design brief here, not a blank one you write from scratch.
2. Identify specifically what's underperforming, using the critique lens from [references/review-and-audit.md](../references/review-and-audit.md) (weak hierarchy, inconsistent spacing, repetitive composition, unclear communication) — scoped to what the user actually asked about, not a full redesign-grade critique unless they asked for one.
3. Make the smallest change set that fixes the named problem, extending the project's existing tokens/conventions rather than forking a parallel system next to them.
4. Verify the change didn't regress anything outside its scope — run the relevant parts of [references/review-and-audit.md](../references/review-and-audit.md) at least around the changed area, more broadly if the change touched shared tokens.

## Acceptance criteria

- The change is scoped to what was asked; nothing outside that scope was "also" redesigned.
- Existing tokens/conventions were extended, not duplicated or forked.
- The site's established identity (brand voice, signature elements, IA) is unchanged.
- If, partway through, the right fix turns out to require a broader change than "refine" implies, say so explicitly and confirm before expanding scope — don't quietly turn a refine request into a redesign.
