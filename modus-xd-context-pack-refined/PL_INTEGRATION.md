# Product Context Pack Integration Guide

This file defines how the XD context pack should connect to the Product Context Pack.

The goal is clean ownership. Product Leadership should remain the authority for product direction, value, prioritization, release learning, and adoption. XD should add the experience implementation context that makes the intended product buildable, testable, and reviewable.

## Shared Product Spine

Use the Product Context Pack for:

| Product Context Pack File | Owner | XD Contribution |
|---|---|---|
| 01_business_intent.md | Product Leadership | Add user outcome and behavior-change language where needed. |
| 02_value_flow_map.md | Product Leadership | Add experience friction, task success, and usability signals. |
| 03_requirement_hierarchy.md | Product Leadership | Add experience references, UX acceptance, and sandbox links to features/epics/stories. |
| 04_decision_log.md | Shared, Product-led | Add discipline tag: Product, XD, Engineering, QE, Data, AI. |
| 06_release_learning_map.md | Product Leadership | Add usability findings, experience QA findings, and sandbox-to-build deltas. |
| 07_adoption_scorecard.md | Product Leadership | Add leading behavior indicators and friction measures. |
| 09_backlog_export_ready.md | Product Leadership | Add experience reference fields and UX readiness status. |
| 10_prompt_library.md | Shared | Add XD prompts for flow review, sandbox review, accessibility, and interaction behavior. |

The XD extension layer files and their purposes are listed in `README.md` (Document Purposes). This guide covers only how those files connect to the Product Context Pack.

## Non-Duplication Rules

Do not create a second version of:

- business intent
- strategic objectives
- financial model
- prioritization rationale
- roadmap sequencing
- release learning
- adoption scorecard
- decision log

Reference those artifacts and add the experience details needed for execution.

## Backlog Integration Standard

Every experience-heavy feature, epic, or story should reference:

- product intent from the Product Context Pack
- relevant experience-context file(s)
- sandbox route, state, or branch
- interaction behavior expectations
- component or pattern guidance
- content/copy source
- accessibility expectations
- instrumentation events or measurement signals
- UX acceptance criteria
- open questions or known experience debt

## Shared Decision Log Tags

Use one shared decision log with discipline tags.

Recommended tags:

```text
[Product]
[Experience]
[Engineering]
[QE]
[Data]
[AI]
[Accessibility]
[Content]
[Measurement]
[Architecture]
[Scope]
```

Decision format:

```text
### Decision: [Short decision name]

**Date:** [YYYY-MM-DD]
**Status:** Proposed / Decided / Changed / Superseded
**Tags:** [Experience], [Product], [Engineering]
**Owner:** [Name]

**Decision:** [What was decided]

**Rationale:** [Why this direction was selected]

**Options considered:**
1. [Option]
2. [Option]
3. [Option]

**Tradeoffs:** [What we gain and lose]

**Downstream implications:** [Backlog, sandbox, system, data, QA, launch]

**Open questions:** [What remains unresolved]
```

## Recommended Product Pack Edits

Add these fields to Product Context Pack templates when the work is experience-heavy.

### Feature Template Additions

```text
Experience Hypothesis:
Target user behavior:
Primary task success metric:
Friction signal:
Instrumentation needed:
Experience mode:
Experience risks:
Validation method:
```

### Epic Template Additions

```text
Primary flow / walking skeleton:
Experience Sandbox reference:
Key states represented:
Role / permission implications:
Experience acceptance criteria:
Known experience debt:
```

### User Story Template Additions

```text
Experience Reference:
- Sandbox route/state/branch:
- Figma frame, if required:
- Context files:
- Interaction states covered:
- Content/copy source:
- Accessibility expectations:
- Instrumentation events:
- UX acceptance:
```

### Jira/Linear Field Additions

```text
Design Mode
Experience Reference URL
Sandbox Route
UX Acceptance Criteria
Accessibility Requirement
Content Source
Instrumentation Event
Measurement Hypothesis
Experience QA Status
Design Debt
```

## Working Standard

A ticket does not need to contain every line of context. It must explicitly link to the canonical context files and sandbox references that define the work. The ticket should make clear what matters, what can change, and what must not drift.
