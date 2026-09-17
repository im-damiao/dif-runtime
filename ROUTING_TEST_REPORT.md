# Routing Test Report

## Scope

Conceptual validation of intent resolution, Primary Mode routing, context gating, dependency resolution, and Routing Trace guidance.

## Results

| Test | Input | Interpreted Intent | Primary Mode | Supporting Modules | Skipped Relevant Modules | Blocking Unknowns | Approval Gates | Expected Runtime Behavior | Pass / Fail | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 01 | Briefing do Product Manager | Analyze Brief | 10 Analyze Brief | None | UI Design | Material brief gaps only | None | Analyze before solution design. | Pass | Minimum execution. |
| 02 | Abandonment before redesign | Discovery | 11 Discovery | None | UI Design | Research evidence if required | None | Investigate before redesign. | Pass | No visual solution. |
| 03 | Password recovery flow | User Flow | 12 User Flow | None | Wireframe, UI Design | Goal and constraints if unavailable | None | Define flow only. | Pass | No visual output. |
| 04 | Approved flow to wireframes | Wireframe | 13 Wireframe | User Flow only if absent | UI Design | Approved flow if unavailable | None | Verify flow first. | Pass | Conditional dependency. |
| 05 | Approved wireframes to final UI | UI Design | 14 UI Design | Wireframe only if structure is absent | Discovery, Handoff | Design source only when required | Design System governance | Inspect context before UI work. | Pass | No invented system. |
| 06 | Interface review before development | Design Review | 15 Design Review | Accessibility or DS Review only when justified | None by default | Review evidence if unavailable | None | Do not load all reviews automatically. | Pass | Final Validation is conditional. |
| 07 | Accessibility requirements | Accessibility Review | 16 Accessibility Review | None | Discovery, Wireframe | Material accessibility evidence | None | Evaluate accessibility only. | Pass | Scope preserved. |
| 08 | DS compliance of a screen | Design System Review | 17 DS Review | Discovery only if context is absent | UI Design | DS identity when required for finding | None | Inspect evidence before asking. | Pass | No assumed library. |
| 09 | New reusable component request | Component Creation | 18 Component Creator | DS Review only if needed for gap | UI Design | Gap evidence if unavailable | Confirmed gap and explicit request or approval | Author only under policy. | Pass | Request is explicit; gap still required. |
| 10 | Approved screens to development | Handoff | 19 Handoff | Final Validation only when required | Creation workflows | Approved artifacts if unavailable | None | Verify handoff prerequisites. | Pass | No redesign. |
| 11 | Validation before implementation | Final Validation | 22 Final Validation | Only gate-required checks | Creation workflows | Validation-scope evidence | None | Validate readiness. | Pass | No unrelated workflow. |
| 12 | Product decisions to PRD | PRD | 23 PRD Generator | None | UI Design | Decisions if required | None | Generate PRD only. | Pass | No UI creation. |
| 13 | Structured solution critique | Design Critique | 24 Design Critique | None | Design Review | Material artifact context | None | Critique the solution. | Pass | Distinct intent. |
| 14 | Post-project learnings | Retrospective | 25 Retrospective | None | Creation workflows | Project evidence if material | None | Record learnings. | Pass | Post-project mode. |
| 15 | Improve this screen | Ambiguous | None until resolved | Context inspection only | UI Design | Material intent ambiguity | None | Ask after evidence inspection only. | Pass | No default UI Design. |
| 16 | Analyze a user flow; no Workspace | User Flow | 12 User Flow | None | Workspace initialization | None solely from absent Workspace | None | Continue with material available. | Pass | Record limitations. |
| 17 | Final UI; no identifiable DS | UI Design | 14 UI Design | DESIGN.md discovery | DS Review unless needed | Design source if no validated local pattern | DS governance | Do not invent DS; ask only if blocking. | Pass | Conditional block. |
| 18 | Brief, flow, then wireframes | Sequential request | 10 → 12 → 13 | Prior completed mode input | UI Design | Gates between stages | None | Execute stated sequence only. | Pass | No added UI Design. |
| 19 | Component consistency with identified DS | DS Review | 17 DS Review | None | Library selection question | None with one official source | None | Use identified source. | Pass | Evidence first. |
| 20 | Accessibility only; do not alter layout | Accessibility Review | 16 Accessibility Review | None | Design Review, UI Design | Material accessibility evidence | None | Do not alter layout or expand scope. | Pass | Scope limit honored. |

## Out of Scope Findings

- agents/04-workspace-context.md requires Workspace context before every design task, while routing requires task-specific context gating. It was not changed because this stage prohibits edits to core modules without explicit review.
- Existing workflow modules may recommend next workflows. This routing layer treats recommendations as optional follow-ups unless a gate or request makes them required.

## Content Preservation

No changes were made to DESIGN.md, agents/00-system.md through agents/04-workspace-context.md, agents/10-analyze-brief.md through agents/25-retrospective.md, or MIGRATION_REPORT.md.
