# Experience Story Extension

Use this section inside Jira, Linear, or a markdown backlog story when the work has a visual, interaction, flow, content, accessibility, or measurement impact.

## Story Header

**Story ID:** [ID]

**Story name:** [Name]

**Parent epic:** [Epic]

**Primary role:** [Specific role]

**Design mode:** Mode 1 / Mode 2 / Mode 3

**Experience readiness status:** Not ready / Ready with risk / Ready

## User Story

```text
As a [specific role],
I want to [specific action],
so that [real user or business outcome].
```

## Experience Reference

**Sandbox route/state/branch:** [Link]

**Figma frame, if required:** [Node-level link]

**Related context files:**
- [Link]
- [Link]

**Related flow ID:** [Flow]

**Related route ID:** [Route]

## Experience Hypothesis

> If we [experience change], then [target user behavior] will improve because [reason].

**Leading signal:** [Signal]

**Friction signal:** [Signal]

**Instrumentation needed:** [Events/properties]

## Scope

### In Scope

- [Scope item]
- [Scope item]

### Out of Scope

- [Out-of-scope item]
- [Out-of-scope item]

## Interaction States Covered

| State | Included? | Source / notes |
|---|---:|---|
| Default | Yes / No / N/A | [Notes] |
| Loading | Yes / No / N/A | [Notes] |
| Empty | Yes / No / N/A | [Notes] |
| Error | Yes / No / N/A | [Notes] |
| Success | Yes / No / N/A | [Notes] |
| Permission/read-only | Yes / No / N/A | [Notes] |

## Component Guidance

| Component / pattern | Source | Required variant/state | Notes |
|---|---|---|---|
| [Component] | [Library/system] | [Variant] | [Notes] |

## Content Guidance

| Location | Copy | Status | Source |
|---|---|---|---|
| [Location] | [Exact or draft copy] | Draft / Approved / Placeholder | [Source] |

## Accessibility Expectations

- Keyboard behavior: [Expectation]
- Focus behavior: [Expectation]
- Screen reader expectation: [Expectation]
- Contrast/status expectation: [Expectation]
- Responsive expectation: [Expectation]

## Instrumentation Events

| Event | Trigger | Properties | Notes |
|---|---|---|---|
| [event_name] | [Trigger] | [Properties] | [Notes] |

## Acceptance Criteria

```text
AC 1: [Name]

Given [complete starting state and role]
When [specific user action or system event]
Then [observable result]
And [state, copy, timing, accessibility, or instrumentation expectation if relevant]
```

Repeat for each AC.

## Open Questions

| Question | Owner | Needed by | Status |
|---|---|---|---|
| [Question] | [Owner] | [Date/gate] | Open / Resolved |

## Known Experience Debt

| Debt item | Risk | Follow-up | Owner |
|---|---|---|---|
| [Debt] | [Risk] | [Link] | [Owner] |

## Readiness Checklist

- [ ] Specific role and outcome are defined.
- [ ] Experience reference is linked and current.
- [ ] Flow and route context are named.
- [ ] Interaction states are covered or explicitly out of scope.
- [ ] Components/patterns are named.
- [ ] Content is exact where needed.
- [ ] Accessibility expectations are stated.
- [ ] Instrumentation is defined when behavior change is expected.
- [ ] Acceptance criteria are observable and testable.
- [ ] Open questions do not block implementation, or are explicitly accepted as risk.
