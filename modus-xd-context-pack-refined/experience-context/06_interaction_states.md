# 06 - Interaction States

## Metadata

**Project:** [Project / product name]  
**XD Owner:** [Name]  
**Engineering Contributor:** [Name]  
**QE Contributor:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  

## Purpose

Define how the product behaves across states, transitions, validation, errors, permissions, confirmations, recovery paths, and edge cases.

This file is critical for agentic delivery. Static screens are not enough. Engineers and agents need behavior rules that remove guesswork.

**Inherits Modus Experience Standards.** Default state behavior (loading thresholds, empty/error/success/validation/recovery rules) comes from the Modus Experience Standards. Document only the states and behaviors that are specific to this product or differ from the defaults; where a flow follows the defaults, say so rather than restating them.

## Interaction Principles

List specific principles that govern behavior.

### Principle 1: [Name]

**Meaning:** [What this means in the product]

**Implication:** [How it affects states, errors, validation, or feedback]

### Principle 2: [Name]

[Repeat structure]

## Global State Model

| State | Definition | User expectation | System behavior | Example |
|---|---|---|---|---|
| Default | [Definition] | [Expectation] | [Behavior] | [Example] |
| Loading | [Definition] | [Expectation] | [Behavior] | [Example] |
| Empty | [Definition] | [Expectation] | [Behavior] | [Example] |
| Error | [Definition] | [Expectation] | [Behavior] | [Example] |
| Success | [Definition] | [Expectation] | [Behavior] | [Example] |
| Disabled | [Definition] | [Expectation] | [Behavior] | [Example] |
| Read-only | [Definition] | [Expectation] | [Behavior] | [Example] |

## Flow-State Matrix

| Flow / route | Default | Loading | Empty | Error | Success | Recovery | Sandbox link | Story link |
|---|---|---|---|---|---|---|---|---|
| [Flow/route] | [Behavior] | [Behavior] | [Behavior] | [Behavior] | [Behavior] | [Behavior] | [Link] | [Link] |

## Validation Behavior

| Input / action | Validation trigger | Validation rule | Error message | Recovery behavior | Notes |
|---|---|---|---|---|---|
| [Field/action] | On blur / on submit / real-time / server response | [Rule] | [Exact or draft copy] | [Recovery] | [Notes] |

## Error Handling

| Error type | Trigger | User-facing message | System behavior | Recovery path | Severity |
|---|---|---|---|---|---|
| Field error | [Trigger] | [Copy] | [Behavior] | [Recovery] | Low / Med / High |
| Page error | [Trigger] | [Copy] | [Behavior] | [Recovery] | Low / Med / High |
| Permission error | [Trigger] | [Copy] | [Behavior] | [Recovery] | Low / Med / High |
| Network/API error | [Trigger] | [Copy] | [Behavior] | [Recovery] | Low / Med / High |

## Loading Behavior

| Context | Loading indicator | Timing threshold | User can act while loading? | Notes |
|---|---|---|---:|---|
| Page load | [Skeleton/spinner/progress/none] | [Time] | Yes / No | [Notes] |
| Inline action | [Indicator] | [Time] | Yes / No | [Notes] |
| Data refresh | [Indicator] | [Time] | Yes / No | [Notes] |

## Empty State Behavior

| Empty state | Trigger | Message | Primary action | Secondary action | Notes |
|---|---|---|---|---|---|
| [State] | [Trigger] | [Exact or draft copy] | [Action] | [Action] | [Notes] |

## Success and Confirmation Behavior

| Action | Confirmation required? | Success feedback | Duration | Undo/cancel available? | Notes |
|---|---:|---|---|---:|---|
| [Action] | Yes / No | [Feedback] | [Duration] | Yes / No | [Notes] |

## Undo, Cancel, and Recovery

| Action | Can cancel before submit? | Can undo after submit? | Recovery path | Data impact |
|---|---:|---:|---|---|
| [Action] | Yes / No | Yes / No | [Path] | [Impact] |

## Notification Rules

| Notification type | When used | Placement | Dismissal | Copy source | Notes |
|---|---|---|---|---|---|
| Toast | [Use case] | [Placement] | Auto/manual | [Source] | [Notes] |
| Inline alert | [Use case] | [Placement] | Manual/system | [Source] | [Notes] |
| Modal confirmation | [Use case] | [Placement] | User action | [Source] | [Notes] |

## Keyboard and Focus Behavior

`09_accessibility_usability.md` is the single source for accessibility standards (keyboard paths, focus management, screen-reader semantics, contrast, responsive). Use this table only for behavior that is specific to a state or interaction here (e.g., where focus moves after this modal closes or this row is deleted); do not restate general accessibility rules.

| Interaction | Keyboard expectation | Focus behavior | Screen reader expectation | Notes |
|---|---|---|---|---|
| [Interaction] | [Keys] | [Focus behavior] | [Expectation] | [Notes] |

## Role and Permission Behavior

| Role | Interaction | Allowed behavior | Not allowed behavior | UI treatment |
|---|---|---|---|---|
| [Role] | [Interaction] | [Behavior] | [Behavior] | Hidden / disabled / read-only / error |

## Motion and Micro-Interaction Guidance

| Interaction | Motion needed? | Purpose | Constraint |
|---|---:|---|---|
| [Interaction] | Yes / No | [Purpose] | [Constraint] |

## AI Interaction Behavior

Use this section only when the product includes user-facing AI behavior.

| AI behavior | User control | Confidence/uncertainty treatment | Review/approval path | Failure recovery |
|---|---|---|---|---|
| [Behavior] | [Control] | [Treatment] | [Path] | [Recovery] |

## Acceptance Criteria Pattern

Use this format for behavior-specific ACs:

```text
**AC [#]: [Behavior name]**

Given [complete state and role]
When [specific user action or system event]
Then [observable result]
And [state, copy, timing, focus, or recovery expectation]
And [instrumentation or test expectation if relevant]
```

## Assumptions and Open Questions

- **[Assumption]** [Statement]
- **[Open question]** [Question]
- **[Needs validation]** [Validation item]

## Agent Guidance

- Do not invent states or error behavior.
- Use exact copy from `08_content_language.md` when available.
- Use this file before generating acceptance criteria, UI logic, or tests.
- If a route has no documented error/empty/loading behavior, mark it as an open question.

## Quality Standard

This file is ready when every experience-heavy story can reference clear behavior rules for states, validation, errors, loading, empty states, permissions, confirmations, and recovery.

## Related Documents

- Journeys and Flows: `03_journeys_flows.md`
- IA and Object Model: `04_ia_object_model.md`
- Content and Language: `08_content_language.md`
- Accessibility and Usability: `09_accessibility_usability.md`
