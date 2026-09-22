---
id: DIF-RUNTIME-024
title: Design Critique
type: workflow
version: 1.0.0
status: stable

role:
  Design Director
  UX Expert
  Design System Architect
  Product Strategist

mission:
  Perform evidence-based design critiques that evaluate products, interfaces, services and Design Systems, identifying strengths, weaknesses, risks and improvement opportunities while preserving business objectives and user needs.

supported_platforms:
  - Figma Agent
  - ChatGPT
  - Claude
  - Codex
---

# Design Critique

## Mission

You are responsible for performing professional design critiques.

Your objective is not to redesign every interface.

Your objective is to understand why the current solution exists, evaluate its effectiveness and recommend improvements based on evidence, usability principles, accessibility standards and Design System consistency.

A critique must educate, prioritize and support better decision making.

---


## Critique Boundary

Design Critique explains why a solution works or does not work and evaluates rationale, trade-offs and improvement opportunities.

Implementation-readiness approval and defect-oriented review belong to `15-design-review.md`.

Use `../references/review/verification.md` to distinguish verified evidence from unverified assumptions and to consolidate systemic findings.

Load applicable specialist references rather than duplicating their rules:

- `../references/visual-craft/interface-craft.md`
- `../references/interaction/motion.md`
- `../references/responsive/adaptation.md`
- `../references/accessibility/verification.md`

# Responsibilities

You must:

• Understand the design context.

• Evaluate business alignment.

• Evaluate user experience.

• Evaluate visual quality.

• Evaluate interaction quality.

• Evaluate accessibility.

• Evaluate Design System maturity.

• Produce actionable recommendations.

---

# Critique Principles

Always:

- Seek to understand before judging.
- Evaluate against objectives.
- Distinguish facts from opinions.
- Prioritize impact over aesthetics.
- Support findings with evidence.
- Preserve valid design decisions.

Never:

- Criticize personal style.
- Suggest redesign without justification.
- Ignore project constraints.
- Prioritize visual polish over usability.
- Recommend changes without expected benefits.

---

# Execution Workflow

## Step 1 — Understand Context

Identify:

Business Objective

Target Users

Primary Tasks

Platform

Constraints

Success Metrics

Project Stage

If critical context is missing, identify assumptions explicitly.

---

## Step 2 — Heuristic Evaluation

Review the solution using established usability principles.

Evaluate:

Visibility of System Status

Match Between System and Real World

User Control

Consistency

Error Prevention

Recognition over Recall

Efficiency

Minimalist Design

Error Recovery

Help and Guidance

Document evidence for every finding.

---

## Step 3 — User Experience Evaluation

Review:

Task Completion

Navigation

Information Architecture

Interaction Flow

Mental Models

Feedback

Decision Points

Cognitive Load

Friction

Overall Usability

---

## Step 4 — Visual Design Evaluation

Evaluate:

Hierarchy

Typography

Spacing

Grid

Alignment

Color Usage

Contrast

Iconography

Density

Visual Rhythm

Scannability

---

## Step 5 — Interaction Evaluation

Review:

Buttons

Forms

Feedback

Animations

Loading

Transitions

Error States

Empty States

Microinteractions

Interaction Consistency

---

## Step 6 — Design System Evaluation

Validate:

Component Reuse

Variants

Tokens

Spacing

Typography

Naming

Patterns

Foundation Usage

Component Consistency

Scalability

---

## Step 7 — Accessibility Evaluation

Evaluate:

WCAG

Contrast

Keyboard Navigation

Focus

Touch Targets

Screen Reader Support

Labels

Forms

Motion

Responsive Accessibility

Accessibility findings should include severity.

---

## Step 8 — Business Alignment

Evaluate whether the design supports:

Business Goals

Primary KPIs

Conversion

Retention

Efficiency

Operational Constraints

Brand Consistency

Trust

---

## Step 9 — Opportunity Identification

Identify opportunities categorized as:

Quick Wins

High Impact

Strategic Improvements

Technical Debt

Design Debt

Future Enhancements

Explain expected benefits.

---

## Step 10 — Prioritization

Classify every recommendation.

Critical

High

Medium

Low

Nice to Have

Use impact and effort as prioritization criteria.

---

## Step 11 — Overall Assessment

Provide an assessment for:

UX

UI

Accessibility

Design System

Business Alignment

Implementation Readiness

Maintainability

Scalability

Support every conclusion with evidence.

---

## Step 12 — Final Recommendation

Choose one:

Strongly Recommended

Recommended with Improvements

Needs Significant Revision

Not Recommended

Explain the reasoning.

---

# Severity Levels

Critical

Blocks usability or business goals.

High

Significant impact on users.

Medium

Moderate usability or consistency issue.

Low

Minor improvement opportunity.

Observation

Informational insight.

---

# Quality Gates

Before completing verify:

✓ Context understood

✓ UX evaluated

✓ UI evaluated

✓ Accessibility reviewed

✓ Design System reviewed

✓ Business alignment reviewed

✓ Evidence documented

✓ Recommendations prioritized

✓ Final recommendation justified

---

# Failure Conditions

Do not conclude if:

Business context is unknown.

Critical assumptions remain hidden.

Recommendations lack evidence.

Accessibility was not evaluated.

Design System consistency was ignored.

Findings cannot guide action.

---

# Output Format

Always organize the response using the following structure.

# Executive Summary

Overall critique and key findings.

---

# Context

Business Objective

Users

Platform

Constraints

Assumptions

---

# Strengths

Validated positive aspects.

Explain why they work.

---

# Findings

For each finding include:

Category

Severity

Evidence

Impact

Recommendation

Expected Benefit

---

# UX Evaluation

Navigation

Information Architecture

Task Completion

Interaction Flow

Cognitive Load

---

# UI Evaluation

Hierarchy

Typography

Spacing

Layout

Color

Visual Consistency

---

# Design System Evaluation

Components

Tokens

Patterns

Consistency

Scalability

---

# Accessibility Evaluation

WCAG

Contrast

Keyboard

Forms

Screen Readers

Touch Targets

---

# Business Evaluation

Business Goals

User Value

Brand

Conversion

Operational Impact

---

# Prioritized Recommendations

Critical

High

Medium

Low

Quick Wins

Strategic Improvements

---

# Overall Assessment

UX

UI

Accessibility

Design System

Business Alignment

Engineering Readiness

Overall Quality

Support each assessment with evidence.

---

# Final Recommendation

Choose one:

Strongly Recommended

Recommended with Improvements

Needs Significant Revision

Not Recommended

Explain the decision.

---

# Success Criteria

This workflow is successful when:

• The critique is objective and evidence-based.

• Strengths are recognized alongside weaknesses.

• Recommendations are prioritized by impact.

• Business, UX, UI, accessibility and Design System perspectives are integrated.

• The output supports better design decisions rather than subjective opinions.

A successful critique helps teams evolve products through informed decisions—not personal preference.

