# 03 - Journeys and Flows

## Metadata

**Project:** [Project / product name]  
**XD Owner:** [Name]  
**Product Owner:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  
**Related Product Context:** [Link to Product Context Pack]  

## Purpose

Define the product paths that users must move through to complete meaningful work. This file captures hero flows, secondary flows, edge cases, service dependencies, state changes, and flow-specific acceptance expectations.

For Mode 1, this file should be tight enough to guide the Experience Sandbox and backlog. For Mode 2 and 3, it should also support stakeholder approval, design system governance, and release readiness.

## Flow Summary

| Flow ID | Flow name | Primary role | Business/user outcome | Priority | Sandbox coverage | Backlog link |
|---|---|---|---|---|---|---|
| F-001 | [Flow] | [Role] | [Outcome] | P0 / P1 / P2 | Full / Partial / None | [Link] |

## Hero Flow

### Flow ID: F-001

**Flow name:** [Name]

**Primary role:** [Role]

**User outcome:** [Outcome]

**Business outcome:** [Outcome]

**Entry point:** [Where the user starts]

**Exit point:** [What counts as completion]

**Related product KR / metric:** [Link or ID]

**Related sandbox route(s):** [Routes]

### Flow Steps

| Step | User action | System response | Data/object involved | State | Decision / rule | Notes |
|---|---|---|---|---|---|---|
| 1 | [Action] | [Response] | [Object] | Default / loading / error / success | [Rule] | [Notes] |
| 2 | [Action] | [Response] | [Object] | [State] | [Rule] | [Notes] |

### Flow Diagram Placeholder

Link to diagram, screenshot, Figma, Miro, sandbox route, or text-based diagram.

```text
[Entry]
  -> [Step]
  -> [Decision]
     -> [Path A]
     -> [Path B]
  -> [Completion]
```

### Acceptance for This Flow

| Acceptance item | Evidence | Owner |
|---|---|---|
| User can complete the flow end to end | [Sandbox / test / story AC] | [Owner] |
| Required states are represented | [Sandbox state / story] | [Owner] |
| Role/permission rules are clear | [Context file / test] | [Owner] |
| Content and labels are final enough for implementation | [Content file / story] | [Owner] |
| Instrumentation is defined | [Measurement file / ticket] | [Owner] |

## Secondary Flows

Use this section for flows that matter but do not define the first release walking skeleton.

### Flow ID: F-002

Repeat the hero flow structure at the level of fidelity required for backlog or sandbox work.

## Edge Cases and Alternate Paths

| Edge case ID | Related flow | Trigger | Expected behavior | User message | Severity | Backlog link |
|---|---|---|---|---|---|---|
| EC-001 | F-001 | [Trigger] | [Behavior] | [Exact or draft copy] | Low / Med / High | [Link] |

## Failure Paths

| Failure path | Trigger | System response | User recovery path | Measurement signal | Owner |
|---|---|---|---|---|---|
| [Failure] | [Trigger] | [Response] | [Recovery] | [Signal] | [Owner] |

## Empty, Loading, and Success Paths

| Flow | Empty state | Loading state | Success state | Error state |
|---|---|---|---|---|
| [Flow] | [Expectation] | [Expectation] | [Expectation] | [Expectation] |

## Cross-Role Handoffs

| Handoff | Flow step | From role | To role | Data/object | Notification / signal | Risk |
|---|---|---|---|---|---|---|
| [Handoff] | [Step] | [Role] | [Role] | [Object] | [Signal] | [Risk] |

## Service and System Dependencies

| Dependency | Related flow | What the user sees | What the system needs | Risk |
|---|---|---|---|---|
| [System/API/service] | [Flow] | [Visible impact] | [Need] | [Risk] |

## Sandbox Coverage Matrix

| Flow | Route(s) | States covered | States missing | Decision needed |
|---|---|---|---|---|
| [Flow] | [Route] | [States] | [Missing] | [Decision] |

## Flow Measurement

| Flow | Success signal | Friction signal | Instrumentation event(s) | Review cadence |
|---|---|---|---|---|
| [Flow] | [Signal] | [Signal] | [Events] | [Cadence] |

## Assumptions and Open Questions

- **[Assumption]** [Statement]
- **[Open question]** [Question]
- **[Needs validation]** [Validation item]

## Agent Guidance

When creating stories, tests, or implementation tasks:

- Preserve the flow order unless a decision log entry changes it.
- Do not skip recovery paths for high-impact failure states.
- Do not invent alternate paths without adding them to this file.
- Link stories to flow IDs and sandbox routes.

## Quality Standard

This file is ready when each critical user journey has a defined entry, completion point, major steps, state expectations, edge cases, and sandbox/backlog coverage.

## Related Documents

- Users, Tasks, Roles: `02_users_tasks_roles.md`
- IA and Object Model: `04_ia_object_model.md`
- Sandbox Manifest: `05_sandbox_manifest.md`
- Interaction States: `06_interaction_states.md`
- Experience Measurement: `11_experience_measurement.md`
