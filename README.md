# GStack — Garry's Stack

**Version:** v1.58.3.0  
**Status:** Active Development  
**Repository:** https://github.com/OneByJorah/gstack

---

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Technology Stack](#technology-stack)
- [Features](#features)
- [Getting Started](#getting-started)
- [Service Management](#service-management)
- [Project Structure](#project-structure)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## Overview

GStack is a full AI engineering workflow in one repo: Claude Code skills, fast headless browser automation, diagram rendering, PDF generation, decision logs, and artifact management. It provides a CLI-driven stack for code review, browsing, design, and automation.

---

## Architecture

CLI (`bin/*`) → core libraries → headless browser / diagram renderer / PDF engine → workspace output. Skills and rules are defined as `SKILL.md` templates and generated into the rules tree.

Key bundles:
- `autoplan/`, `benchmark/`, `benchmark-models/` skill packs.
- `bin/gstack-*` utilities for analytics, brain/cache, decision logs, community dashboard, and more.
- Extension payload for browser/terminal integration.

---

## Technology Stack

| Layer | Stack |
|---|---|
| Runtime | Node.js / Bun |
| Language | TypeScript / Shell / Python |
| Packaging | npm / pyproject.toml |
| Build | bash scripts / bun |
| Browser | Headless automation (browse CLI / CDP) |
| Docs | Markdown skill docs generator |
| VCS | Git + GitHub (`github.com/OneByJorah/gstack`) |

---

## Features

- **Codex-ready skills**: autocoded SKILL.md templates for plan, benchmark, autoplan, and more.
- **Headless browser**: fast browse CLI with CDP and extension support.
- **Diagram + PDF**: render diagrams and generate PDFs.
- **Decision log**: `gstack-decision-log` / `gstack-decision-search` for traceability.
- **Artifacts**: `gstack-artifacts-*` for init, URL, and analytics.
- **Community dashboard**: `gstack-community-dashboard` for usage/feedback.
- **Multi-mode**: supports `npm run build`, `npm run dev`, and `npm run server`.

---

## Getting Started

```bash
# 1. Clone
git clone https://github.com/OneByJorah/gstack.git
cd gstack

# 2. Install
npm install
# or
bun install

# 3. Build
npm run build

# 4. Run browser
npm run dev
# or start server
npm run server
```

See `ARCHITECTURE.md` and individual `bin/` tool READMEs for sub-command docs.

---

## Service Management

```bash
# Development
npm run dev          # browse CLI
npm run server       # server mode

# Build/publish artifacts
npm run build
```

---

## Project Structure

```
gstack/
├── bin/               # Executable CLIs (browse, gstack-*, make-pdf, etc.)
├── autoplan/
├── benchmark/
├── benchmark-models/
├── docs/
├── extension/         # Browser extension payload + icons
├── lib/               # Shared libs (browser, diagram-render)
├── agents/
├── agents/*.yaml
├── AGENTS.md
├── ARCHITECTURE.md
├── package.json
└── README.md
```

---

## Screenshots

### GitHub UI Reference
![GitHub 2013](docs/images/github-2013.png)

### GitHub UI Reference
![GitHub 2026](docs/images/github-2026.png)

### Extension Icon
![Icon](extension/icons/icon-128.png)

---

## Contributing

1. Create a feature branch off `main`.
2. Build and test affected CLI tools before submitting.
3. Submit a PR with description and screenshots for UI changes.

---

## License

MIT

---

## Author

Built by **Jhonattan L. Jimenez**.
