# DIF × Figma Agent

## Status

Validated experimental adapter for Figma Agent.

## Purpose

Provide a single designer-facing entry point for the DIF Runtime in Figma Agent.

The user invokes:

`/dif <natural-language request>`

The adapter interprets the request and selects the applicable DIF Primary Mode internally. The designer does not need to choose or attach individual runtime modules.

## Validated Architecture

```
Designer
  ↓
/dif
  ↓
DIF routing + method + governance
  ↓
Figma Agent native execution capabilities
  ↓
Active Design System
  ↓
Artifact
  ↓
/dif review / validation
```

Responsibilities are intentionally separated:

- **DIF Runtime:** intent, method, UX criteria, accessibility governance, Design System governance, evidence discipline, gates, validation and escalation.
- **Figma Agent:** canvas manipulation, inspection and other native execution capabilities.
- **Design System:** actual foundations, variables, styles, components, variants and patterns.
- **Human:** consequential Product, business, architecture and Design System decisions.

The adapter must not hardcode a company-specific Design System.

## Why a Single Entry Point

Native automatic discovery of independently installed DIF Custom Skills was not reliable in the controlled lab. Individual workflows worked when explicitly invoked, but repeated natural-language creation tests returned that no DIF Custom Skill had been used.

Therefore automatic Custom Skill routing is not a dependency of this integration.

The stable interaction model is explicit invocation of one entry point: `/dif`.

## Lab Evidence

Validated behaviors:

1. Figma Agent can use a connected mature Design System for interface creation.
2. DIF UI Design rules materially improve Design System reuse.
3. DIF Design Review can inspect a created artifact and identify local recreation, foundation/style gaps and implementation-readiness issues.
4. DIF Accessibility Review works as a specialized method and may be complemented by native Figma auditing capabilities.
5. A single `/dif` adapter can route a natural-language creation request to UI Design behavior and a subsequent evaluation request to Design Review behavior.
6. Creator self-report is not accepted as compliance evidence; post-creation inspection is required.

## Accessibility Boundary

Native audit results are supporting evidence, not normative authority.

The adapter uses WCAG 2.2 AA as fallback when the project does not define another target and includes guardrails against known interpretation errors, including:

- no invented generic 12px WCAG minimum font size;
- SC 1.4.12 treated as Text Spacing;
- SC 2.5.8 treated as 24 × 24 CSS pixels or its defined exceptions, not the 44 × 44 AAA threshold from SC 2.5.5;
- no automatic equivalence between Figma design pixels and CSS pixels without implementation evidence;
- runtime keyboard, semantics, screen-reader behavior and production responsiveness marked as unverifiable from static design evidence when applicable.

## Source of Truth

The modular DIF Runtime remains canonical.

This adapter is a compiled execution surface for Figma Agent, not a replacement for the runtime modules.

Changes to DIF methodology should be made in the canonical Runtime first and then reconciled into this adapter.

## Installation

Install `adapters/figma-agent/SKILL.md` as a Figma Agent Custom Skill.

Keep the relevant Design System connected separately through Figma's Design Libraries.

Individual DIF workflow Custom Skills are not required for the single-entry workflow.

## Usage

Examples:

```
/dif Crie uma interface desktop para gestão de contratos...
```

```
/dif Avalie esta interface antes de encaminhá-la para desenvolvimento. Não altere a interface.
```

```
/dif Faça uma auditoria de acessibilidade desta interface.
```

The request remains natural language. Module numbers are an implementation detail of the Runtime.

## Governance

The adapter must:

- ask only for blocking unknowns;
- inspect evidence before assuming;
- prefer the active official Design System;
- reuse confirmed applicable official components;
- require approval for consequential Design System changes;
- distinguish verified evidence from insufficient evidence;
- validate materialized output rather than trust creator claims;
- escalate Product/business/architecture decisions when required.

## Lab Result

The personal Figma lab validated the integration hypothesis:

**DIF can operate as the method/governance layer above Figma Agent while the active Design System remains the implementation source of truth.**

The remaining production concern is lifecycle synchronization between the canonical modular Runtime and this compiled single-file adapter.
