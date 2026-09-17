---
id: DIF-RUNTIME-003
title: Component & Design System Policy
type: runtime-core
version: 1.0.0
status: stable

depends_on:
  - DIF-RUNTIME-000
  - DIF-RUNTIME-001
  - DIF-RUNTIME-002

target:
  - Figma Agent
  - ChatGPT
  - Claude
  - Codex
---

# Component & Design System Policy

## Mission

Guarantee that every UI generated, modified or reviewed by the Runtime follows Design System governance before introducing new interface elements.

The Runtime must always prefer consistency over originality.

---

# Design System Detection

Before manipulating any interface determine:

- Is there a Design System?

Possible answers:

• Yes

• No

• Unknown

If Unknown:

Stop.

Ask the user.

Never assume.

---

# Library Selection

First inspect available project evidence to identify the Design System and active library.

If the active library can be identified reliably:

Use it.

If multiple valid libraries remain and the choice affects the result:

Ask the user which Design System library should be used.

If no library can be identified after inspection:

Ask the user for context.

If no Design System exists:

Do not invent one. Use validated local patterns when appropriate and register Design System gaps.

Never mix libraries automatically unless that composition is officially defined by the project.

Evidence before clarification.

Ask only when ambiguity materially affects execution.

---

# Active Library Rule

After the active library is identified or confirmed:

Treat that library as the single source of truth.

Never mix components from different libraries unless that composition is officially defined by the project.

---

# Component Discovery

Before creating anything search for:

- Foundations
- Design Tokens
- Icons
- Components
- Variants
- Patterns
- Templates

If an existing solution satisfies the requirement:

Reuse it.

Do not recreate it.

---

# Foundations First

Whenever creating or modifying UI always verify:

## Colors

Use existing color tokens.

Never create arbitrary colors.

---

## Typography

Use existing typography styles.

Never create custom font scales.

---

## Spacing

Use spacing tokens whenever available.

Avoid arbitrary spacing values.

---

## Radius

Reuse existing corner radius tokens.

---

## Elevation

Reuse elevation and shadow tokens.

---

## Icons

Reuse the official icon library.

Do not mix icon families.

---

# Component Reuse Policy

Always follow this priority:

1 Existing Component

↓

2 Existing Variant

↓

3 Existing Pattern

↓

4 Confirmed Gap

↓

5 Component Proposal

↓

6 Human Approval

↓

7 Component Creation

Reuse before creating.

Proposal before structural change.

Human approval before Design System evolution.

---

# New Component Policy

If no reusable component exists:

1. Confirm the gap with evidence.
2. Verify whether an existing variant or pattern resolves the requirement.
3. Document the gap.
4. Propose a reusable solution.
5. Identify the impact on the Design System.
6. Recommend creation when appropriate.
7. Do not create a structural component automatically.
8. Enter Component Authoring Mode only when component creation is explicitly requested or approved.

The proposal or approved component should define:

- Name
- Category
- Purpose
- Description
- Variants
- Properties
- States
- Auto Layout
- Responsive behavior
- Accessibility notes
- Usage examples

---

# Naming Convention

When creating components use:

Component / Subcomponent / Variant

Examples:

Button / Primary

Input / Password

Card / Product

Modal / Confirmation

Avoid ambiguous names.

Avoid abbreviations.

---

# Variant Rules

Variants should represent:

- Size
- State
- Appearance
- Interaction

Avoid creating unnecessary variants.

---

# Component States

Every interactive component should consider:

- Default
- Hover
- Focus
- Pressed
- Disabled
- Loading
- Error
- Success

Never document only the default state.

---

# Auto Layout Policy

Every new component should support Auto Layout whenever applicable.

Verify:

- padding
- spacing
- alignment
- resizing
- hugging
- filling

Avoid fixed layouts unless required.

---

# Accessibility Requirements

Every new component should verify:

- WCAG contrast
- Keyboard navigation
- Focus visibility
- Touch targets
- Screen reader labels
- Error feedback

Accessibility is mandatory.

---

# Documentation Requirements

Whenever a new reusable component is created generate:

Purpose

Usage

Do

Don't

Variants

Properties

Accessibility Notes

Related Components

---

# Design System Evolution

Whenever a reusable component is created evaluate:

Should this become part of the Design System?

If yes:

Recommend inclusion.

Explain why.

---

# Runtime Output

Whenever component decisions occur include:

## Library Used

## Existing Components Reused

## New Components Created

## Foundations Used

## Tokens Used

## Accessibility Notes

## Documentation Recommendations

---

# Runtime Principle

The Runtime should contribute to the continuous evolution of the Design System.

It should never increase inconsistency.
