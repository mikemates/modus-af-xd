# 00 - Experience Mode

## Metadata

**Project:** [Project / product name]  
**Client:** [Client name]  
**XD Owner:** [Name]  
**Product Owner:** [Name]  
**Engineering Lead:** [Name]  
**QE Lead:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  
**Related Product Context:** [Link to Product Context Pack]  

## Purpose

Define the design operating mode for this product and the working model the team will use to move from product intent to build-ready experience context.

This file prevents process ambiguity. It clarifies how much Figma, sandbox, research, brand, design system, and review governance are required for this initiative.

## Selected Mode

**Selected Mode:** Mode 0 / Mode 1 / Mode 2 / Mode 3

**Mode name:** [Opportunity Definition / Code-First Product Shaping / Brand-Aware Accelerated MVP / Design-System Governed Delivery]

**Decision date:** [YYYY-MM-DD]

**Decision owner:** [Name]

**Approvers:** [Product, XD, Engineering, Client]

## Mode Rationale

### Why this mode fits

[Explain why this is the lightest responsible workflow for the product, audience, brand, system maturity, and delivery context.]

Use direct language:

- The product is [greenfield / brownfield / modernization / extension].
- The audience is [internal / B2B / B2C / mixed].
- Brand risk is [low / moderate / high].
- Design system maturity is [none / lightweight / component library / mature governed system].
- Working software is [more / equally / less] valuable than static fidelity at this stage.
- The experience risk is [low / moderate / high] because [reason].

### Why other modes were not selected

| Mode | Why not selected |
|---|---|
| Mode 0 | [Reason] |
| Mode 1 | [Reason] |
| Mode 2 | [Reason] |
| Mode 3 | [Reason] |

## Mode Selection Criteria

| Criterion | Current state | Implication |
|---|---|---|
| Product maturity | [Opportunity / known solution / extension / modernization] | [Mode implication] |
| Greenfield or brownfield | [Answer] | [Mode implication] |
| User complexity | [Narrow / mixed / broad / regulated] | [Mode implication] |
| Role and permission complexity | [Low / moderate / high] | [Mode implication] |
| Brand importance | [Minimal / moderate / critical] | [Mode implication] |
| Design system maturity | [None / library / mature system] | [Mode implication] |
| Client approval expectations | [Figma-first / prototype-first / build-first / mixed] | [Mode implication] |
| Compliance/accessibility risk | [Low / moderate / high] | [Mode implication] |
| Speed to working software | [Low / moderate / high priority] | [Mode implication] |
| Cost of experience drift | [Low / moderate / high] | [Mode implication] |

## Role of Figma

**Figma status:** Not required / Optional / Required for selected flows / Required source of truth

### Figma will be used for

- [Flow sketching]
- [IA exploration]
- [Brand-critical screens]
- [Design system mapping]
- [Stakeholder approval]
- [Other]

### Figma will not be used for

- [Reasonably omitted artifact]
- [Reasonably omitted artifact]

### Figma requirement by flow or screen

| Flow / screen | Figma required? | Reason | Link |
|---|---:|---|---|
| [Flow] | Yes / No | [Why] | [URL] |

## Role of Experience Sandbox

**Sandbox status:** Not used / Supporting reference / Primary experience reference

**Sandbox repository or location:** [URL]

**Sandbox owner:** [XD owner]

**Engineering review owner:** [Engineering lead]

### Sandbox will demonstrate

- [Primary flow]
- [Route structure]
- [State behavior]
- [Representative data]
- [Interaction pattern]
- [Other]

### Sandbox will not demonstrate

- [Out-of-scope behavior]
- [Production integration]
- [Architecture decision]
- [Other]

## Required Context Files

| File | Required? | Owner | Due | Status |
|---|---:|---|---|---|
| 01_experience_intent.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 02_users_tasks_roles.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 03_journeys_flows.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 04_ia_object_model.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 05_sandbox_manifest.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 06_interaction_states.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 07_components_patterns.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 08_content_language.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 09_accessibility_usability.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 10_experience_acceptance.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 11_experience_measurement.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 12_research_validation.md | Yes / No | [Name] | [Date] | Draft / Ready |
| 13_ai_experience_patterns.md | Yes / No | [Name] | [Date] | Draft / Ready |

## Intentionally Omitted Artifacts

| Artifact | Why omitted | Risk | Mitigation |
|---|---|---|---|
| [Artifact] | [Reason] | [Risk] | [Mitigation] |

## Review Cadence

| Review | Participants | Cadence | Purpose |
|---|---|---|---|
| Experience direction review | Product + XD | [Cadence] | Confirm intent, flows, and priorities. |
| Sandbox review | Product + XD + Engineering | [Cadence] | Confirm feasibility and build readiness. |
| Backlog readiness review | Product + XD + Engineering + QE | [Cadence] | Confirm stories are AI-ready. |
| Experience QA | XD + QE + Engineering | [Cadence] | Review built software against intent. |
| Learning review | Product + XD + Data/QE | [Cadence] | Review adoption, friction, and improvement signals. |

## Approval Expectations

| Gate | Required approval | Evidence |
|---|---|---|
| Product direction | Product + XD | Product Context Pack + experience intent |
| Sandbox readiness | XD + Engineering | Sandbox manifest + review notes |
| AI-ready backlog | Product + XD + Engineering + QE | Story extension + readiness gate |
| Experience acceptance | XD + Product + QE | QA checklist + accepted debt |

## Escalation Triggers

Escalate when:

- The selected mode no longer matches product risk.
- Client requires Figma approval that was not planned.
- Brand or design system expectations increase.
- Accessibility, compliance, or role complexity increases.
- The sandbox is being treated as production code without engineering review.
- Agents or engineers are inventing layout, state behavior, copy, or user intent.
- Major implementation divergence from sandbox is not documented.

## Quality Standard

This file is ready when a new team member can understand the intended design workflow, required artifacts, review model, and risk boundaries without asking for process clarification.

## Related Documents

- Product Context Pack: [Link]
- Experience Intent: `01_experience_intent.md`
- Sandbox Manifest: `05_sandbox_manifest.md`
- AI Readiness Gate: `../templates-and-standards/experience_ai_readiness_gate.md`
- Shared Decision Log: [Link]
