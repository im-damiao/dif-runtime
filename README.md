# Design Intelligence Framework (DIF)

Portable, versioned Design Intelligence Runtime for Product Design, UX, UI, Design Systems and AI-assisted design workflows.

## Distributions

The repository contains two clearly separated ways to use DIF.

### 1. DIF Runtime — complete

Path: `skills/dif-runtime/`

Use this distribution with Codex and compatible agents that can access the modular Runtime.

It contains:

- `SKILL.md` — canonical Runtime entry point and orchestrator.
- `DESIGN.md` — universal design-context discovery protocol.
- `agents/` — permanent rules and specialized modules 10–25.

The modular Runtime remains the canonical source of DIF methodology and governance.

### 2. DIF Figma Agent — /dif

Path: `adapters/figma-agent/`

Use this distribution inside Figma Agent.

Install `adapters/figma-agent/SKILL.md` as a Custom Skill. The designer uses one entry point:

```
/dif <natural-language request>
```

The adapter routes the request internally. Individual DIF module numbers do not need to be selected by the designer.

The active Figma Design Library remains separate from DIF and supplies the actual foundations, variables, styles, components, variants and patterns.

See `adapters/figma-agent/README.md` for installation, architecture and validated lab behavior.

## Workspace

Organization-specific context belongs in `workspace/WORKSPACE.md`, based on `workspace/WORKSPACE.example.md`.

Keep Workspace context private. Do not hardcode a company-specific Design System, product or confidential context into the portable Runtime.

## Repository Structure

```
dif-runtime/
├── skills/
│   └── dif-runtime/          # DIF Runtime — complete/canonical
│       ├── SKILL.md
│       ├── DESIGN.md
│       └── agents/
├── adapters/
│   └── figma-agent/          # DIF Figma Agent — /dif
│       ├── SKILL.md
│       └── README.md
└── workspace/                # private organization context
```

## Versioning

Repository releases version the complete DIF distribution. Historical tags preserve previous stable states, including `v3.0.0` and `v3.1.0`.
