# 02 - Users, Tasks, and Roles

## Metadata

**Project:** [Project / product name]  
**XD Owner:** [Name]  
**Product Owner:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  
**Related Product Context:** [Link to Product Context Pack]  

## Purpose

Define who the product serves, what they need to accomplish, what roles and permissions shape the experience, and what context of use affects design and implementation.

This file should be specific enough for designers, engineers, QE, and AI agents to understand who is doing what, why, where, and under what constraints.

## User and Role Summary

| Role / user group | Type | Primary goal | Core tasks | Experience priority |
|---|---|---|---|---|
| [Role] | End user / operator / admin / approver / manager / support | [Goal] | [Tasks] | [Clarity / speed / control / trust / compliance] |
| [Role] | [Type] | [Goal] | [Tasks] | [Priority] |

## Primary Users

### [Primary User / Role Name]

**Role description:** [Who they are]

**Business context:** [Where they sit in the organization or service]

**Primary jobs:**
- [Job]
- [Job]
- [Job]

**Common tasks:**
- [Task]
- [Task]
- [Task]

**Success looks like:** [What success means for this user]

**Pain points:**
- [Pain]
- [Pain]

**Expertise level:** Novice / trained operator / domain expert / administrator / mixed

**Frequency of use:** [Daily / weekly / occasional / exception-based]

**Context of use:**
- Location: [Desk / field / mobile / call center / warehouse / clinic / other]
- Device: [Desktop / tablet / mobile / scanner / mixed]
- Time pressure: [Low / moderate / high]
- Interruption risk: [Low / moderate / high]
- Collaboration: [Solo / paired / handoff / cross-team]

**Accessibility considerations:** [Known needs, risk areas, or assumed baseline]

**Design implications:**
- [Implication]
- [Implication]

## Secondary Users

Repeat the primary user structure for secondary users, approvers, support teams, managers, admins, or downstream consumers.

## Role and Permission Model

| Role | Can view | Can create | Can edit | Can approve | Can delete | Can export | Notes |
|---|---|---|---|---|---|---|---|
| [Role] | [Objects/pages] | [Objects] | [Objects] | [Objects] | [Objects] | [Objects] | [Notes] |

## Task Inventory

| Task ID | Task | Primary role | Trigger | Frequency | Current friction | Desired outcome | Related flow |
|---|---|---|---|---|---|---|---|
| T-001 | [Task] | [Role] | [Trigger] | [Frequency] | [Friction] | [Outcome] | [Flow] |

## Task Criticality

| Task | Criticality | Why it matters | Failure impact | Design implication |
|---|---|---|---|---|
| [Task] | Must-have / should-have / nice-to-have | [Reason] | [Impact] | [Implication] |

## Cross-Role Handoffs

| Handoff | From | To | Object / data passed | Decision needed | Risk |
|---|---|---|---|---|---|
| [Handoff] | [Role] | [Role] | [Object/data] | [Decision] | [Risk] |

## Mental Models and Terminology

| User term | System term | Recommended product term | Notes |
|---|---|---|---|
| [Term users say] | [Backend/system term] | [UI term] | [Why] |

## User Constraints

| Constraint | Affected roles | Design implication | Implementation implication |
|---|---|---|---|
| [Constraint] | [Roles] | [Design] | [Implementation] |

## Assumptions and Unknowns

### Assumptions

- **[Assumption]** [User behavior or role assumption]
  - Risk if wrong: [Risk]
  - Validation method: [Method]

### Open Questions

- **[Open question]** [Question]
  - Owner: [Name]
  - Needed by: [Gate]

## Agent Guidance

When generating UI, stories, tests, or implementation plans:

- Use the specific role names in this file, not generic "user" labels.
- Do not invent permissions or visibility rules.
- Do not assume all roles can perform all actions.
- Ask for clarification if a task, role, or handoff is not represented.

## Quality Standard

This file is ready when each major flow can be traced to a specific role, task, context of use, and permission expectation.

## Related Documents

- Experience Intent: `01_experience_intent.md`
- Journeys and Flows: `03_journeys_flows.md`
- IA and Object Model: `04_ia_object_model.md`
- Content and Language: `08_content_language.md`
