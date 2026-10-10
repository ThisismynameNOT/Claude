# Performance and SEO

## Performance

Prioritize the critical content and interactions. Avoid shipping large images, fonts, animation packages, and third-party scripts without a reason. Use responsive image delivery, correct dimensions, lazy loading for offscreen media, and appropriate loading priority for the actual main content. Preserve layout space for media and embeds to reduce shifts.

When field measurement is relevant, use current Core Web Vitals guidance. The current “good” thresholds are LCP ≤ 2.5 seconds, INP ≤ 200 milliseconds, and CLS ≤ 0.1 at the 75th percentile, segmented by mobile and desktop. Treat them as outcome targets, not a guarantee from code inspection. Field data needs sufficient representative traffic; lab data is useful for diagnosis but is not field evidence.

Use profiling or Lighthouse/PageSpeed/DevTools where available. Record environment, route, device profile, and whether the value is field or lab data. Do not invent measurements or promise that a refactor will improve a metric without testing.

## Public-site SEO

For indexable public pages, verify descriptive titles and metadata, canonical URLs when needed, crawlable links, heading/content structure, indexability, and meaningful image alt text. Add structured data only when the page genuinely qualifies and the data is accurate. Do not add SEO elements to private admin or authenticated pages as if they were public landing pages.

Protect noindex, robots, preview, canonical, and authentication behavior when editing existing routes. Do not expose draft or private content through metadata, sitemaps, or public assets.

## Sources

- [web.dev: Web Vitals](https://web.dev/articles/vitals)
- [web.dev: defining Core Web Vitals thresholds](https://web.dev/articles/defining-core-web-vitals-thresholds)
