---
id: DIF-RUNTIME-004
title: Workspace Context
type: runtime-core
version: 1.0.0
status: stable

depends_on:
  - DIF-RUNTIME-000
  - DIF-RUNTIME-001
  - DIF-RUNTIME-002
  - DIF-RUNTIME-003

target:
  - Figma Agent
  - ChatGPT
  - Claude
  - Codex
---

# Workspace Context

## Mission

This document defines the design environment where the Runtime operates.

It centralizes organization-specific rules without changing Runtime behavior.

The Runtime must read this context before executing any design task.

---

# Runtime Initialization

Before executing any task determine:

✓ Platform

✓ Product

✓ Design System

✓ Component Library

✓ Foundations

✓ Tokens

✓ Naming Convention

✓ Accessibility Level

✓ Responsive Targets

✓ Documentation Standard

If any mandatory information is unavailable, ask the user.

Never assume.

---

# Organization Context

Organization:

Project:

Product:

Business Domain:

Design Maturity:

---

# Platform

Possible values:

- Web
- Mobile
- Desktop
- Responsive
- Multi-platform

Multiple selections allowed.

---

# Design Tool

Possible values:

- Figma
- Penpot
- Sketch
- Adobe XD

Default:

Figma

---

# Design System

Design System Name:

Version:

Owner:

Documentation URL:

Status:

- Stable
- Beta
- Experimental

---

# Component Libraries

For each available library register:

Library Name:

Purpose:

Owner:

Version:

Status:

Priority:

Example:

Library:

Omnilab Core

Purpose:

Main Product Components

Priority:

Primary

---

# Foundations

Register available foundations.

Examples:

Colors

Typography

Spacing

Grid

Radius

Elevation

Motion

Icons

Illustrations

---

# Design Tokens

If available register:

Color Tokens

Spacing Tokens

Typography Tokens

Radius Tokens

Shadow Tokens

Motion Tokens

---

# Naming Convention

Document standards for:

Pages

Frames

Sections

Components

Variants

Properties

Variables

Tokens

Assets

---

# Accessibility Standard

Possible values:

WCAG AA

WCAG AAA

Internal Standard

Additional Notes:

---

# Responsive Targets

Supported breakpoints:

Desktop

Tablet

Mobile

Large Displays

Other

---

# Component Governance

Should the Runtime:

Reuse components?

Create components?

Suggest Design System evolution?

Generate documentation?

Generate variants?

Possible answers:

Yes / No

---

# Publishing Policy

When new reusable components are created:

Publish automatically?

No.

Always suggest.

Human approval required.

---

# Documentation Standard

When generating documentation include:

Purpose

Usage

Variants

Properties

Accessibility

Examples

Do

Don't

Related Components

Implementation Notes

---

# AI Behavior Overrides

The organization may define additional rules.

Examples:

Prefer enterprise patterns.

Avoid experimental layouts.

Never introduce custom colors.

Always prefer existing tokens.

Never publish components automatically.

---

# Runtime Initialization Checklist

Before execution verify:

✓ Workspace identified

✓ Platform identified

✓ Design System selected

✓ Library selected

✓ Foundations available

✓ Naming available

✓ Accessibility defined

✓ Documentation standard available

---

# Runtime Context Output

Whenever a new task begins summarize:

Platform

Design System

Library

Foundations

Accessibility Target

Component Strategy

Documentation Strategy

This summary becomes the execution context for the remaining workflow.

