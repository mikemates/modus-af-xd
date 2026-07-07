# XD Context Pack Prompt Library

Use these prompts with Claude, ChatGPT, Cursor, Codex-style agents, or other AI tools. Replace bracketed placeholders before use.

## 1. Mode Selection

```text
Review the project context below and recommend the appropriate design operating mode: Mode 0, Mode 1, Mode 2, or Mode 3.

Assess product maturity, user complexity, brand importance, design system maturity, delivery urgency, client approval expectations, accessibility/compliance risk, and cost of experience drift.

Output:
- recommended mode
- rationale
- risks
- required context files
- role of Figma
- role of Experience Sandbox
- escalation triggers

Context:
[Paste context]
```

## 2. Experience Intent Draft

```text
Using the Product Context Pack and notes below, draft `01_experience_intent.md`.

Focus on target user behavior, user outcomes, experience hypothesis, experience principles, what must not drift, assumptions, open questions, and measurement implications.

Do not duplicate business intent. Reference it and translate it into experience behavior.

Inputs:
[Paste links or text]
```

## 3. Users, Tasks, and Roles Review

```text
Review `02_users_tasks_roles.md` for specificity.

Flag:
- generic user labels
- missing roles
- missing permissions
- unclear tasks
- missing context of use
- accessibility implications
- handoffs that need documentation

Output a readiness decision and required changes.
```

## 4. Journey and Flow Decomposition

```text
Turn the following product goal into hero flows, secondary flows, edge cases, and failure paths.

For each flow, include:
- flow ID
- primary role
- entry point
- exit point
- steps
- states
- sandbox coverage needed
- backlog implications
- measurement signals

Product goal:
[Paste goal]
```

## 5. IA and Object Model Review

```text
Review `04_ia_object_model.md` and identify gaps that would cause an engineer or agent to invent structure.

Check for:
- missing routes
- unclear navigation labels
- undefined objects
- undefined object relationships
- status/state ambiguity
- missing permissions
- search/filter/sort gaps
- terminology drift
```

## 6. Sandbox Manifest Generation

```text
Using the sandbox routes and context files below, draft or update `05_sandbox_manifest.md`.

Map:
- sandbox routes to flows
- routes/states to epics/stories
- states covered and missing
- mock data coverage
- reusable candidates
- reference-only elements
- engineering review notes
- open questions

Inputs:
[Paste route list, file tree, notes]
```

## 7. Interaction State Gap Review

```text
Review the following flow or story for missing interaction states.

Check default, loading, empty, error, success, validation, permission, confirmation, undo/cancel, retry, keyboard, focus, and accessibility behavior.

Return:
- missing states
- required ACs
- copy needs
- accessibility needs
- open questions

Flow/story:
[Paste content]
```

## 8. Experience AI Readiness Review

```text
Evaluate this story against the Experience AI Readiness Gate.

Return:
- Ready / Ready with risk / Not ready / Blocked
- missing product/user context
- missing experience reference
- missing state behavior
- missing component guidance
- missing content/copy
- missing accessibility expectations
- missing instrumentation
- rewritten acceptance criteria if needed

Story:
[Paste story]
```

## 9. Experience QA Review

```text
Review this implemented build against the XD context pack.

Assess:
- flow completion
- IA/navigation
- interaction behavior
- components/patterns
- content clarity
- error/loading/empty states
- accessibility
- responsive behavior
- instrumentation
- design debt

Inputs:
[Paste build notes/screenshots/context]
```

## 10. Release Learning Capture

```text
Summarize experience learnings from this release and propose updates to the context pack.

Capture:
- what changed from sandbox
- what changed from original intent
- what usability/accessibility issues emerged
- what behavior signals changed
- what should become reusable pattern guidance
- what should become design debt or backlog

Inputs:
[Paste release notes, QA findings, analytics]
```
