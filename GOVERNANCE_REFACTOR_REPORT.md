# Governance Refactor Report

## Scope

Normalize only the two Design System and component-governance conflicts documented in MIGRATION_REPORT.md.

## Files Changed

- skills/dif-runtime/agents/03-component-policy.md
- VERSION
- CHANGELOG.md
- GOVERNANCE_REFACTOR_REPORT.md

## Conflict 01

### Previous Rule

Always ask which Design System library should be used and never choose automatically.

### Normalized Rule

Inspect project evidence first. Use a reliably identified active library; ask only when multiple valid libraries create material ambiguity or no library can be identified after inspection. When no Design System exists, do not invent one; use validated local patterns when appropriate and register gaps.

### Reason

Aligns the policy with 01-runtime-rules.md Rule 03 and 02-decision-tree.md Steps 03–04.

### Impact

Eliminates unnecessary clarification while preserving protection against unsupported assumptions and automatic library mixing.

## Conflict 02

### Previous Rule

The absence of a reusable component could lead directly to creation of a scalable component.

### Normalized Rule

Existing Component → Existing Variant → Existing Pattern → Confirmed Gap → Component Proposal → Human Approval → Component Creation.

### Reason

Aligns the policy with 01-runtime-rules.md Rule 04, 02-decision-tree.md Step 06, and DESIGN.md sections 14 and 24.

### Impact

Structural component creation now requires documented evidence, a proposal, and an explicit request or approval.

## Cross Validation

| Reference | Result |
| --- | --- |
| 00-system.md | Consistent with reuse before creation, evidence-based decisions, and validation. |
| 01-runtime-rules.md | Consistent with evidence-based library identification and approval before component creation. |
| 02-decision-tree.md | Consistent with Design System detection, library selection, component lookup, and authoring-mode entry. |
| DESIGN.md | Consistent with source-of-truth discovery, no invented Design System, and gap documentation before component creation. |

## Scenario Validation

| Scenario | Result |
| --- | --- |
| A — one identifiable active library | Use it without unnecessary confirmation. |
| B — multiple valid libraries with no scope evidence | Request confirmation. |
| C — no Design System | Do not invent one; use validated local patterns where appropriate and register gaps. |
| D — existing official component | Reuse it. |
| E — existing variant resolves requirement | Reuse the variant before proposing a component. |
| F — no component, variant, or pattern | Confirm and document the gap; create a proposal; do not create automatically. |
| G — explicit approval | Component Authoring Mode may be entered under existing DIF policies. |

## Out of Scope Findings

- 03-component-policy.md retains its existing example library names. They were not changed because organizational-example cleanup is outside this refactor scope.

## Content Preservation

IDs, metadata, mission, general file structure, accessibility rules, naming rules, component states, Auto Layout policy, documentation requirements, runtime output format, and unrelated rules were preserved. Workflows 10–25, SKILL.md, DESIGN.md, Workspace, and MIGRATION_REPORT.md were not changed.
