# Quality rubric

Use only when a scored review is useful. Rate each applicable category 1–5, cite evidence, and mark unavailable evidence **unscored**. Adjust weights for the product mode when justified; never hide a hard failure in a weighted total.

| Category | Default weight | Evidence to review |
|---|---:|---|
| Art direction and originality | 20% | Fit to brand/audience, specific visual rationale, lack of arbitrary decoration |
| Usability and information architecture | 15% | Task clarity, hierarchy, navigation, error recovery |
| Visual coherence and typography | 15% | Consistent type, color, spacing, component language |
| Motion and interaction quality | 10% | Purpose, input support, interruption, reduced motion |
| Responsive implementation | 10% | Checked widths, reflow, overflow, interaction adaptation |
| Accessibility | 10% | Semantics, keyboard, focus, contrast, errors, reduced motion |
| Engineering quality and performance | 10% | Preserved contracts, maintainability, measured/runtime evidence |
| Content authenticity and business effectiveness | 10% | Verified claims/assets, clear user value and primary action |

## Rating anchors

- **1 — Fails:** blocks a key task or lacks evidence for a required dimension.
- **2 — Weak:** substantial defects or inconsistencies remain.
- **3 — Adequate:** works for the main case, with material gaps or limited coverage.
- **4 — Strong:** coherent and well verified, with only localized improvement needs.
- **5 — Excellent:** unusually clear, robust, distinctive, and supported by broad relevant evidence.

Do not score based on screenshots alone when functionality is in scope. Do not treat the absence of measured field data as proof of poor performance; mark it unscored or state that only lab evidence exists.

## Hard gates outside the score

Report separately and do not average away:

- security, privacy, or data-integrity issue;
- core task or route broken;
- fabricated business claim or unauthorized asset;
- keyboard-inaccessible essential interaction;
- critical content obscured, clipped, or unavailable;
- known severe motion or flashing hazard.

## Report format

State scope and evidence, then category ratings with a short rationale, hard gates, unscored areas, and prioritized next actions. If weights change, show the revised weights. If no meaningful evidence exists, provide findings without a numeric total.
