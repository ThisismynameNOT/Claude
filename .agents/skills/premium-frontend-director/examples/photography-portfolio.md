# Example: Premium Photography Portfolio (Experience mode)

## Brief

"An immersive portfolio site for a photographer — the work should be the focus, not the UI."

## How the Skill should work it

**Mode**: Experience — the interface recedes, the imagery leads from the first viewport.

**Dials**: `DESIGN_VARIANCE` can run high if the sequencing is intentional (8-10: full-bleed, asymmetric image pairing), `MOTION_INTENSITY` mid-high but restrained in character — transitions should feel like turning a page, not like a marketing demo reel. `VISUAL_DENSITY` low — the images need room; UI chrome (nav, captions, metadata) should be minimal and quiet.

**Typography**: editorial, not interface-style — this is one of the clearer cases for a genuinely distinctive display face and generous type scale, per [references/typography-and-color.md](../references/typography-and-color.md); restraint applies to UI labels and captions, not to the editorial type carrying the work itself.

**Motion** (per [references/motion-and-interactions.md](../references/motion-and-interactions.md)): image transitions are the one place in this build where "explanation/delight" purpose is legitimately central, since the mode is Experience. Still run the frequency gate — a gallery viewed sequentially many times in one session still shouldn't ship a transition so long it becomes an obstacle; keep crossfades/slides snappy enough not to fight repeat viewing, and ensure `prefers-reduced-motion` still produces a usable (instant-cut) experience.

**Content authenticity**: every image is the photographer's actual work — no stock placeholders standing in as if they were the photographer's images; if real images aren't yet supplied, build the structure with explicit placeholder markers rather than filling galleries with stock photography that would misrepresent the body of work.

**Signature element**: tied to this photographer's actual style — a particular sequencing rhythm, a consistent crop/aspect language across the grid, or a caption/metadata treatment that reflects how they actually talk about their work (a landscape photographer's EXIF-forward metadata reads very differently from a portrait photographer's minimal captions).

## What "done" looks like

Fast, high-quality image delivery (correctly sized/optimized per [references/performance-and-seo.md](../references/performance-and-seo.md) despite being an image-heavy site), keyboard-navigable gallery, real images throughout, and a UI that genuinely gets out of the way rather than competing with the photography for attention.
