# DIF — Figma Agent Role Profiles

DIF uses one canonical methodology with role-specific execution profiles.

## Coordinator

Current full adapter: `adapters/figma-agent/SKILL.md`

The coordinator retains the full DIF Figma Agent execution surface and the human authority to make or authorize structural decisions when supported by evidence.

## Designer

Profile: `adapters/figma-agent/designer/SKILL.md`

The Designer profile keeps DIF reasoning, Design System discipline, accessibility, UI creation, review, documentation, and handoff capabilities. Structural Design System changes, product-wide patterns, consequential flow/Product decisions, architecture decisions, and final organizational approval are routed to coordinator review.

## Distribution

- Coordinator installs `adapters/figma-agent/SKILL.md`.
- Designers install `adapters/figma-agent/designer/SKILL.md`.
- Both invoke the skill with `/dif`.
- Install only the profile appropriate to the person's role.

## Principle

Restrict authority, not reasoning quality.

The modular Runtime under `skills/dif-runtime/` remains the canonical source of DIF methodology.
