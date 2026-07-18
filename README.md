# Draw.io Diagram Skill

Generate editable draw.io / diagrams.net diagrams from natural-language requests, with local export, validation, fallback links, and layout guidance for architecture, flow, UML, ERD, BPMN, network, C4, and report-style diagrams.

## What It Does

- Creates `.drawio` XML diagrams that remain editable in draw.io / diagrams.net.
- Exports PNG, SVG, PDF, or JPG locally through draw.io Desktop.
- Supports precise hand-authored XML, Mermaid-to-drawio conversion, and data-driven generators.
- Includes helpers for architecture diagrams, sequence diagrams, C4, ERD, OpenAPI, Terraform, Kubernetes, CI, heat maps, and more.
- Provides validation, troubleshooting, PNG repair, browser fallback links, and report-style layout rules.

## Requirements

Install draw.io Desktop for local export. The diagrams.net web app alone is not enough for local CLI export.

macOS:

```bash
brew install --cask drawio
drawio --version
```

If Homebrew or command-line downloads are slow, download draw.io Desktop manually from GitHub Releases:

<https://github.com/jgraph/drawio-desktop/releases>

Choose the installer for your OS:

- macOS: `.dmg`
- Windows: `.exe`
- Linux: `.deb` or `.rpm` (avoid snap when possible)

Graphviz is optional and only needed for some auto-layout workflows:

```bash
brew install graphviz
```

## Installation

Copy the whole repository folder into your Codex skills directory:

```bash
~/.codex/skills/drawio-diagram-skill/
```

Do not copy only `SKILL.md`. The `scripts/`, `references/`, `styles/`, and `data/` folders are part of the workflow.

## Fallback Behavior

If the draw.io CLI is unavailable or crashes in a sandboxed environment, the skill can still produce `.drawio` XML and diagrams.net edit links. Local PNG/SVG/PDF export may need to be done outside the sandbox.

## License

MIT
