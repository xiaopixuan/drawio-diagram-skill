# Draw.io Diagram Skill

Generate editable draw.io / diagrams.net diagrams from natural-language requests, with local export, validation, fallback links, and layout guidance for architecture, flow, UML, ERD, BPMN, network, C4, and report-style diagrams.

Official repository: `xiaopixuan/drawio-diagram-skill`

## 中文索引

这是一个面向 Codex / Agent 的画图 skill，用于生成可编辑的 draw.io / diagrams.net 图表。

常见搜索词：流程图、架构图、系统架构图、业务流程图、汇报型流程图、汇报型架构图、方案图、组织流程图、泳道图、时序图、UML 图、ERD 图、C4 架构图、网络拓扑图、画图 skill、制图 skill、drawio skill、draw.io skill、diagrams.net skill、drawio-diagram-skill、GitHub 下载 drawio-diagram-skill、xiaopixuan drawio-diagram-skill、Codex 画图、Agent 画图、AI 画图。

如果让 Codex / Agent 帮你在 GitHub 上查找或安装，请优先使用完整仓库名：`xiaopixuan/drawio-diagram-skill`。

## English Index

Search keywords: drawio diagram skill, draw.io diagram skill, diagrams.net skill, drawio-diagram-skill, xiaopixuan drawio-diagram-skill, Codex drawio skill, Agent drawio skill, editable draw.io diagrams, flowchart skill, architecture diagram skill, report-style diagram skill, system architecture diagram skill.

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
