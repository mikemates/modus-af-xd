# Agent Instructions for the XD Context Pack

Use this file to guide AI agents working with the XD context pack, Product Context Pack, Experience Sandbox, and backlog.

## System Context

This repository contains experience implementation context. It defines how the product should behave from a user, flow, IA, interaction, component, content, accessibility, measurement, and acceptance perspective.

This repository does not replace:

- Product Context Pack
- technical architecture
- production code standards
- QE test strategy
- client governance requirements

## Required Reading Order

Before acting on experience-heavy work, read:

1. Product Context Pack business intent and requirement hierarchy
2. `experience-context/00_experience_mode.md`
3. `experience-context/01_experience_intent.md`
4. `experience-context/02_users_tasks_roles.md`
5. `experience-context/03_journeys_flows.md`
6. `experience-context/04_ia_object_model.md`
7. `experience-context/05_sandbox_manifest.md` if a sandbox exists
8. `experience-context/06_interaction_states.md`
9. `experience-context/07_components_patterns.md`
10. `experience-context/08_content_language.md` if content matters
11. `experience-context/09_accessibility_usability.md`
12. `experience-context/10_experience_acceptance.md`
13. `experience-context/11_experience_measurement.md` if behavior change is expected

## Operating Rules

- Do not invent user roles, permissions, routes, object names, state behavior, copy, or accessibility rules.
- Use the selected design mode to determine the required experience reference.
- In Mode 1, use sandbox routes/states as the primary experience reference when available.
- In Mode 2, use sandbox plus brand/content/Figma guidance where required.
- In Mode 3, use Figma and design system mapping as the primary source of visual/system truth.
- Treat sandbox code as reference-only unless engineering has marked it reusable.
- Mark unresolved items as `[Open question]`, `[Assumption]`, or `[Needs validation]`.
- Preserve existing decisions unless a linked decision log entry changes them.
- If context conflicts, stop and ask which source is authoritative.

## When Generating Backlog Items

Author against the `../templates-and-standards/experience_story_extension.md` template and validate with `../templates-and-standards/experience_ai_readiness_gate.md`. Include:

- specific role
- user/job context
- flow ID
- route ID
- experience reference link
- interaction states
- component guidance
- content/copy source
- accessibility expectations
- instrumentation events if needed
- observable acceptance criteria
- open questions or accepted debt

## When Generating UI or Sandbox Code

Use:

- approved route structure
- approved component library
- approved terminology
- documented states
- representative mock data
- accessibility expectations
- clear comments for simplified behavior

Do not:

- create production architecture
- introduce new patterns without documenting them
- rely on color alone for status
- hide errors or recovery paths
- add AI behavior without checking `13_ai_experience_patterns.md`

## Review Output Format

For gated reviews, apply the shared checks in `../templates-and-standards/experience_quality_review.md` (Sandbox Review and Experience QA) and `../templates-and-standards/experience_ai_readiness_gate.md` (ticket readiness). All three use the same experience quality dimensions.

When reviewing a context file, story, or sandbox, use this format:

```text
## Review of [item]

### Strengths
- [What is clear]

### Gaps
- [Missing or unclear context]

### Risks
- [Implementation, usability, accessibility, measurement, or drift risk]

### Required changes before ready
- [Change]

### Suggested improvements
- [Improvement]

### Readiness decision
Ready / Ready with risk / Not ready / Blocked
```

## Quality Standard

Agent output should reduce ambiguity. If the output creates new hidden assumptions, it is not ready.
