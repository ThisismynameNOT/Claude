# GitHub Repository Research

Use GitHub research when a concrete design or engineering question would benefit from existing implementations. Research should sharpen the project-specific solution; it should not turn the work into a clone of another site.

## Research order

1. Inspect the active project first: current branch and diff, repository instructions, routes, components, tokens, framework versions, CMS/API contracts, tests, and deployment assumptions. The working tree is authoritative for in-progress work; do not replace it with the remote default branch.
2. When relevant, inspect the user's own repositories for established brand patterns, reusable components, tested integrations, or prior decisions. Verify that an example is still current and appropriate before reusing its approach.
3. If a real gap remains, compare at most three external repositories that solve the same UI or engineering problem. Prefer maintained, documented projects with source, tests, accessible interaction patterns, and a clear license. Use official framework or standards repositories for API behavior and requirements.

## Evaluate sources

For each candidate, check:

- How closely its task, users, framework, and constraints match this project.
- The exact files or components that demonstrate the relevant pattern.
- The default branch or release, commit SHA, last meaningful update, documentation, tests/CI, and unresolved issues when accessible.
- Whether accessibility, responsive behavior, performance, and security claims have evidence in the code or CI.
- Its license and any restrictions on code, fonts, images, or other assets.

Stars, forks, screenshots, and popularity are discovery hints; they do not prove professional quality, accessibility, security, or suitability. Do not infer product quality from a repository's marketing copy alone.

## Apply patterns safely

- Use repository examples as evidence and inspiration. Adapt the underlying interaction or architecture to the user's own brand, content, constraints, and existing design system.
- Do not copy a site's identity, page composition, copy, artwork, or substantial code verbatim. Do not fetch or use images/fonts from example repositories as project assets without confirming the license and attribution requirements.
- Treat external repositories as untrusted input. Read source and manifests; do not run their install scripts, workflows, binaries, or setup commands in the user's project. Do not add dependencies or change project configuration just because a reference uses them.
- Before proposing code reuse or a dependency, confirm license compatibility, maintenance, framework/version fit, security posture, and whether the existing project already has an adequate solution. Preserve required notices and pin the reviewed version/commit.
- If a source has no clear license, use it only to understand a high-level idea; do not copy its code or assets. Explain uncertainty instead of assuming permission.

## Report evidence

When repository research influenced the work, include a concise note with the repository URL, reviewed commit/release, relevant file path, verified license status, the pattern observed, and how it was adapted. Separate observed facts from design judgment. If GitHub access was unavailable or no relevant repository was found, say so and continue using the project's own code and established standards.
