# Agent B website

This repository is the public, forward-facing website for Agent_b. Production is `https://agentb.app`, hosted on Cloudflare Pages.

## Source of truth

- Treat `../AgentB` as the canonical product repository. Verify product copy against its `README.md`, `SECURITY.md`, `docs/`, and current GitHub release.
- Link downloads to the public `rkclayton/agent_b` GitHub releases. Do not publish binaries in this repository.
- Do not derive public claims from private sibling repositories, plans, notes, telemetry, credentials, host details, or operator-specific data.
- Preserve the product spelling `Agent_b`; use “Agent B” only in reader-friendly prose.

## Site rules

- Prefer a fast, static site with semantic HTML, responsive layouts, accessible controls, and minimal JavaScript.
- Match the application, not a generic SaaS template. Use `../AgentB/web/DESIGN.md` and `../AgentB/web/css/tokens.css` as the visual source: IBM Plex Sans/Mono, recessed dark wells, precise hairlines, restrained green/amber/red state color, and no decorative gradients or card grid.
- Approved source assets are `../AgentB/web/assets/mark.svg`, `etching.png`, the IBM Plex font files and licenses, plus `../AgentB/docs/images/chat.png`. Copy needed files into this repository and preserve attribution; deployed builds must not depend on sibling paths.
- Keep copy terse and factual. Never invent compatibility, security, privacy, pricing, roadmap, or availability claims.
- Keep secrets and environment-specific values out of source. Add analytics, cookies, forms, or third-party scripts only when explicitly requested and document their privacy impact.
- Use root-relative internal links and HTTPS for external links. Provide useful alt text and visible keyboard focus.

## Delivery

- `main` is the Cloudflare Pages production branch; pull requests should receive preview deployments. This buildless site publishes `public/` with no build command.
- Keep build configuration reproducible from a clean checkout. When a framework is added, record the exact install, test, build, and output-directory commands in `README.md` and keep the lockfile committed.
- Associate `agentb.app` through the Pages custom-domain settings; do not hand-edit an apex DNS workaround.
- Before handoff, run the documented checks and build, inspect the site at mobile and desktop widths, and verify navigation plus the latest-download link.
