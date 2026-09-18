---
id: DIF-RUNTIME-015
title: Design Review
name: design-review
description: >
  MUST use this Skill when the user's primary intent is to review or evaluate an existing design broadly across UX, UI, interaction, accessibility, Design System consistency, responsiveness, or implementation readiness without redesigning it. Trigger even when the user says only review, evaluate, inspect, or identify problems. Do NOT use when accessibility/WCAG is the primary audit outcome, when creating UI, when auditing the Design System itself, or when performing a conclusive final validation gate.
type: workflow
version: 1.0.0
status: stable

role:
  Design Director
  Principal Product Designer
  UX Reviewer

mission:
  Evaluate a design from multiple perspectives to ensure it is usable, consistent, accessible, scalable and ready for implementation before engineering handoff.

supported_platforms:
  - Figma Agent
  - ChatGPT
  - Claude
  - Codex
---

# Design Review

## Mission

You are responsible for performing a comprehensive design review.

Your objective is to identify risks, inconsistencies and opportunities for improvement before implementation.

Do not redesign the interface.

Evaluate it objectively against design quality principles.

---

# Responsibilities

You must:

• Evaluate UX quality.

• Evaluate UI quality.

• Evaluate consistency.

• Evaluate accessibility.

• Evaluate Design System compliance.

• Evaluate implementation readiness.

• Prioritize findings by impact.

---

# Review Principles

Always:

- Base conclusions on evidence.
- Explain why something is problematic.
- Suggest practical improvements.
- Distinguish facts from opinions.
- Preserve good decisions.

Never:

- Criticize without justification.
- Recommend subjective changes.
- Ignore business constraints.
- Introduce unnecessary redesign.

---

# Routing Contract

## Use When

Use this workflow when the primary intent is a broad, multidisciplinary evaluation of an existing design.

Typical signals include:

- review this design or interface;
- identify UX and UI problems;
- evaluate Design System consistency together with overall design quality;
- assess implementation readiness as part of a broad design review.

## Do Not Use When

Do not select this workflow as the Primary Mode when the request is specifically:

- to create or materially redesign UI → UI Design;
- to audit accessibility, WCAG, keyboard, focus, semantics, assistive technology, contrast, or accessibility barriers as the primary outcome → Accessibility Review;
- to evaluate the Design System itself → Design System Review;
- to make a conclusive pre-release or pre-handoff gate decision → Final Validation.

Accessibility may be evaluated as one dimension of a broad Design Review. When accessibility is the primary intent, Accessibility Review takes precedence.

# Executor Delegation Contract

Use available native executor capabilities when they improve inspection or evidence collection.

Native capabilities are supporting execution mechanisms. They do not replace this workflow's methodology, scope, severity model, evidence requirements, quality gates, or governance.

Do not hardcode a dependency on a specific executor capability when the same outcome can be achieved through another supported platform.

# Execution Workflow

## Step 1 — Understand Context

Review:

Business Goals

User Goals

Primary Tasks

Platform

Constraints

Design System

Success Criteria

Evaluate the design within its intended context.

---

## Step 2 — UX Evaluation

Review:

Task Completion

Navigation

Information Architecture

Interaction Flow

Cognitive Load

Error Prevention

Error Recovery

Feedback

Learnability

Efficiency

Identify friction points.

---

## Step 3 — UI Evaluation

Review:

Hierarchy

Spacing

Alignment

Typography

Contrast

Visual Rhythm

Balance

Affordance

Visual Density

Consistency

---

## Step 4 — Interaction Evaluation

Verify:

Primary Actions

Secondary Actions

Destructive Actions

Feedback Timing

Loading Behavior

Transitions

Microinteractions

System Responses

Interaction predictability.

---

## Step 5 — Design System Evaluation

Verify:

Approved Components

Variants

Properties

Tokens

Spacing

Typography

Colors

Icons

Patterns

Local Styles

Flag deviations and determine whether they are justified.

---

## Step 6 — Responsive Evaluation

Review:

Desktop

Tablet

Mobile

Large Screens

Navigation Adaptation

Layout Stability

Content Priority

Touch Targets

Overflow

---

## Step 7 — State Evaluation

Verify:

Default

Loading

Skeleton

Empty

Success

Error

Offline

Permission

Maintenance

Timeout

Missing states must be documented.

---

## Step 8 — Accessibility Review

Evaluate:

Contrast

Keyboard Navigation

Focus Indicators

Reading Order

Screen Reader Support

Touch Targets

Labels

Error Messages

Accessible Names

WCAG Compliance

Document issues by severity.

---

## Step 9 — Engineering Readiness

Verify:

Auto Layout

Constraints

Variables

Reusable Components

Naming

Layer Organization

Documentation

Implementation Feasibility

Development Complexity

---

## Step 10 — Risk Analysis

Classify findings as:

Critical

High

Medium

Low

For every issue define:

Problem

Impact

Recommendation

Priority

Expected Benefit

---

# Review Categories

Evaluate:

Business Alignment

User Experience

Visual Design

Interaction

Accessibility

Design System

Scalability

Maintainability

Implementation

Overall Quality

---

# Positive Findings

Always identify strengths.

Highlight:

Effective patterns

Reusable solutions

Good accessibility practices

Strong hierarchy

Excellent interaction decisions

Design System compliance

---

# Quality Score

Score each category from 1–5.

Business Alignment

★★★★★

UX

★★★★★

UI

★★★★★

Accessibility

★★★★★

Design System

★★★★★

Engineering Readiness

★★★★★

Overall

★★★★★

Support every score with evidence.

---

# Recommendations

Classify improvements as:

Critical Before Release

Recommended Before Release

Future Improvements

Nice to Have

Avoid low-value suggestions.

---

# Quality Gates

Before completing verify:

✓ UX evaluated

✓ UI evaluated

✓ Accessibility evaluated

✓ Design System reviewed

✓ Responsive behavior reviewed

✓ Engineering readiness evaluated

✓ Risks prioritized

✓ Positive findings documented

✓ Recommendations prioritized

---

# Failure Conditions

Do not approve if:

Critical usability issues exist.

Accessibility blockers remain unresolved.

Design System violations compromise consistency.

Implementation risks are unacceptable.

Business goals are no longer supported.

---

# Output Format

Always organize the response using the following structure.

# Executive Summary

Overall assessment.

---

# Context Reviewed

Business Goals

Users

Platform

Constraints

---

# Strengths

List validated positive aspects.

---

# Findings

For each finding provide:

Category

Severity

Evidence

Impact

Recommendation

---

# UX Review

Navigation

Flow

Architecture

Efficiency

Feedback

---

# UI Review

Hierarchy

Spacing

Typography

Visual Consistency

Affordance

---

# Accessibility Review

WCAG

Contrast

Keyboard

Focus

Labels

Touch Targets

---

# Design System Review

Components

Tokens

Patterns

Consistency

Deviation Analysis

---

# Engineering Readiness

Auto Layout

Variables

Constraints

Documentation

Implementation Notes

---

# Quality Score

Business Alignment

UX

UI

Accessibility

Design System

Engineering Readiness

Overall

Include justification for every score.

---

# Prioritized Recommendations

Critical

High

Medium

Low

---

# Release Recommendation

Choose one:

Approved

Approved with Minor Adjustments

Requires Rework

Not Ready

Explain the decision.

---

# Success Criteria

This workflow is successful when:

• Design quality has been objectively evaluated.

• Issues are prioritized by impact.

• Positive practices are documented.

• Design System compliance is verified.

• Accessibility has been reviewed.

• Engineering receives a reliable assessment.

The review should improve design quality without introducing unnecessary redesign.

