# copilot-sdk Architectural Dissection

> A comprehensive 14-phase deep dive into [GitHub's copilot-sdk](https://github.com/github/copilot-sdk) — the polyglot SDK powering Copilot integrations across TypeScript, Python, Go, and C#.

[![Live Site](https://img.shields.io/badge/Live_Site-copilot--sdk--dissection.pages.dev-22C55E?style=for-the-badge&logo=cloudflare&logoColor=white)](https://copilot-sdk-dissection.pages.dev)
[![GitHub](https://img.shields.io/github/stars/SufficientDaikon/copilot-sdk-dissection?style=for-the-badge&logo=github)](https://github.com/SufficientDaikon/copilot-sdk-dissection)

---

## What Is This?

An interactive documentation site that methodically analyzes the architecture, patterns, data flows, and internals of GitHub's `copilot-sdk`. Built as a static HTML/CSS/JS site with **87 Mermaid diagrams**, syntax-highlighted code, and a dark-themed UI.

This is **not** official GitHub documentation. It's an independent architectural analysis created to help developers understand how the SDK works under the hood.

## Pages

| # | Phase | What You'll Learn |
|---|-------|-------------------|
| 00 | [Overview](https://copilot-sdk-dissection.pages.dev) | Architecture at a glance, navigation guide |
| 01 | [Discovery](https://copilot-sdk-dissection.pages.dev/01-discovery.html) | Project identity, repo signals, key statistics |
| 02 | [Structure](https://copilot-sdk-dissection.pages.dev/02-structure.html) | Directory layout, module dependencies, layer stack |
| 03 | [Tech Stack](https://copilot-sdk-dissection.pages.dev/03-tech-stack.html) | Languages, build tools, frameworks, IPC architecture |
| 04 | [Entry Points](https://copilot-sdk-dissection.pages.dev/04-entry-points.html) | CLI bootstrap, startup sequences, cross-SDK API table |
| 05 | [Architecture](https://copilot-sdk-dissection.pages.dev/05-architecture.html) | 7 design patterns, state machines, event dispatch |
| 06 | [Data Flow](https://copilot-sdk-dissection.pages.dev/06-data-flow.html) | JSON-RPC flows, sessions, events, tool execution |
| 07 | [API Surface](https://copilot-sdk-dissection.pages.dev/07-api-surface.html) | Public API, method signatures, extension points |
| 08 | [Conventions](https://copilot-sdk-dissection.pages.dev/08-conventions.html) | Naming, error handling, async patterns, code style |
| 09 | [Testing](https://copilot-sdk-dissection.pages.dev/09-testing.html) | Test harness, snapshot system, E2E architecture |
| 10 | [Build & Deploy](https://copilot-sdk-dissection.pages.dev/10-build-deploy.html) | CI/CD pipelines, publishing, CLI bundling |
| 11 | [Dependencies](https://copilot-sdk-dissection.pages.dev/11-dependencies.html) | Runtime + dev dependency analysis per SDK |
| 12 | [Security](https://copilot-sdk-dissection.pages.dev/12-security.html) | Trust boundaries, auth flow, attack surface |
| 13 | [Contribution](https://copilot-sdk-dissection.pages.dev/13-contribution.html) | Code generation pipeline, dev workflows |

## Features

- **87 Mermaid.js diagrams** — flowcharts, sequence diagrams, and state machines that visualize architecture, data flows, and patterns
- **Syntax-highlighted code** — TypeScript, Python, Go, and C# examples with Highlight.js
- **Dark theme** — designed for extended reading with WCAG AA contrast compliance
- **Zero build step** — pure static HTML/CSS/JS, open `index.html` in any browser
- **Responsive** — sidebar navigation collapses on mobile
- **Sequential navigation** — prev/next links across all 14 pages
- **Reading time estimates** — shown on every page

## Tech

| Layer | Choice |
|-------|--------|
| Diagrams | [Mermaid.js v10](https://mermaid.js.org/) (CDN) |
| Syntax Highlighting | [Highlight.js v11.9](https://highlightjs.org/) (CDN) |
| Fonts | JetBrains Mono + IBM Plex Sans (Google Fonts) |
| Hosting | [Cloudflare Pages](https://pages.cloudflare.com/) |
| Build | None — static files only |

## Run Locally

```bash
git clone https://github.com/SufficientDaikon/copilot-sdk-dissection.git
cd copilot-sdk-dissection
# Open in browser — no build needed
open index.html
```

Or use any static server:

```bash
npx serve .
```

## Design

The site uses a consistent dark theme based on these tokens:

| Token | Value | Usage |
|-------|-------|-------|
| `--color-background` | `#0F172A` | Page background |
| `--color-surface` | `#1E293B` | Cards, code blocks |
| `--color-cta` | `#22C55E` | Links, accents |
| `--color-text` | `#F8FAFC` | Primary text |
| `--color-text-dim` | `#7C8BA0` | Secondary text (WCAG AA) |

## Contributing

Found an inaccuracy or want to improve a diagram? PRs welcome.

## License

This is an independent analysis of a public repository. The copilot-sdk itself is owned by GitHub.

---

Built with [Claude Code](https://claude.com/claude-code)
