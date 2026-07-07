# Experience Design Context Pack Navigation Guide

This guide explains how to use the XD context pack across discovery, shaping, sandbox creation, backlog readiness, build, QA, and release learning.

## Navigation Map

```text
START HERE: experience-context/00_experience_mode.md
    -> experience-context/01_experience_intent.md
    -> experience-context/02_users_tasks_roles.md
    -> experience-context/03_journeys_flows.md
    -> experience-context/04_ia_object_model.md
    -> experience-context/05_sandbox_manifest.md
    -> experience-context/06_interaction_states.md
    -> experience-context/07_components_patterns.md
    -> experience-context/08_content_language.md
    -> experience-context/09_accessibility_usability.md
    -> experience-context/10_experience_acceptance.md
    -> experience-context/11_experience_measurement.md
    -> 11_templates_and_standards/experience_ai_readiness_gate.md
    -> experience-sandbox/handoff_notes.md
    -> experience-sandbox/drift_log.md
```

## Document Purposes

### Operating Model

**00_experience_mode.md**
- Which design mode applies?
- Why is that mode responsible for this product?
- What is the role of Figma, sandbox, research, brand, and design system governance?
- What artifacts are required or intentionally omitted?

### Experience Direction

**01_experience_intent.md**
- What user behavior must change?
- What should the experience make easier, faster, clearer, or safer?
- What must not drift during implementation?

**02_users_tasks_roles.md**
- Who uses the product?
- What jobs and tasks matter?
- What roles, permissions, expertise levels, and contexts of use affect the design?

**03_journeys_flows.md**
- What are the hero flows?
- What are the secondary flows, edge cases, handoffs, and failure paths?
- Which flows are covered by the sandbox?

**04_ia_object_model.md**
- How is the product organized?
- What routes, objects, relationships, terminology, filters, and visibility rules matter?

### Sandbox and Build Context

**05_sandbox_manifest.md**
- What does the Experience Sandbox include?
- Which routes, states, flows, and stories does it represent?
- What is reusable, reference-only, or intentionally divergent from production?

**06_interaction_states.md**
- How does the product behave across states, validation, errors, permissions, confirmations, keyboard use, and edge cases?

**07_components_patterns.md**
- What component library or design system is used?
- Which components and patterns are approved, adapted, missing, or debt?

**08_content_language.md**
- What terms, labels, button conventions, error copy, empty states, and tone rules should be used?

### Quality and Learning

**09_accessibility_usability.md**
- What accessibility, usability, responsive, compatibility, and readability expectations apply?

**10_experience_acceptance.md**
- What makes the experience acceptable before demo, release, or handoff?
- What issues block launch versus become accepted debt?

**11_experience_measurement.md**
- What behavior, friction, adoption, and task success signals will show whether the experience is working?

**12_research_validation.md**
- What assumptions need research or validation?
- What evidence is needed before build, release, or scale?

**13_ai_experience_patterns.md**
- What user-facing AI rules apply, including human control, uncertainty, editing, auditability, and trust?

## Required Files by Mode

| File | Mode 0 | Mode 1 | Mode 2 | Mode 3 |
|---|---|---|---|---|
| 00_experience_mode | Required | Required | Required | Required |
| 01_experience_intent | Required | Required | Required | Required |
| 02_users_tasks_roles | Required | Required | Required | Required |
| 03_journeys_flows | Required | Required | Required | Required |
| 04_ia_object_model | Light | Required | Required | Required |
| 05_sandbox_manifest | Optional | Required if sandbox used | Required if sandbox used | Optional/supporting |
| 06_interaction_states | Light | Required | Required | Required |
| 07_components_patterns | Optional | Required | Required | Required |
| 08_content_language | Optional | Recommended | Required | Required |
| 09_accessibility_usability | Required | Required | Required | Required |
| 10_experience_acceptance | Optional | Required | Required | Required |
| 11_experience_measurement | Recommended | Required | Required | Required |
| 12_research_validation | Required | Recommended | Recommended | Recommended |
| 13_ai_experience_patterns | If relevant | If relevant | If relevant | If relevant |

## Using This Pack by Role

### Experience Design

- Own the experience-context files.
- Create and maintain the Experience Sandbox manifest.
- Define interaction behavior, content clarity, accessibility expectations, and UX acceptance.
- Review built software against experience intent.

### Product Leadership

- Own the Product Context Pack.
- Keep business intent, value flow, prioritization, release learning, and adoption scorecard current.
- Partner with XD on experience intent, measurement hypotheses, and AI-ready backlog.

### Engineering

- Use the sandbox and context files as implementation input.
- Decide what sandbox code is reusable versus reference-only.
- Own production architecture, code quality, technical standards, and merge readiness.

### QE

- Use the context pack to design functional, regression, accessibility, and release validation.
- Review acceptance criteria for testability.
- Partner with XD on experience QA and release readiness.

### AI Agents

- Use `agent-instructions/AGENTS.md` before acting.
- Treat context files, sandbox manifest, linked stories, and approved decisions as canonical input.
- Do not invent missing user intent, layout, state behavior, copy, permissions, accessibility rules, or measurement events.

## Pack Review Checklist

Before backlog handoff:

- [ ] Design mode is declared and current.
- [ ] Experience intent references Product Context Pack business intent.
- [ ] Users, tasks, and roles are specific enough for implementation.
- [ ] Hero flows and edge cases are documented.
- [ ] Routes and object model are clear.
- [ ] Sandbox manifest maps routes/states to backlog items.
- [ ] Interaction states are explicit.
- [ ] Components and patterns are named.
- [ ] Content and copy expectations are clear where implementation depends on them.
- [ ] Accessibility expectations are stated.
- [ ] UX acceptance criteria are defined.
- [ ] Instrumentation and measurement expectations are documented.
- [ ] Open questions and accepted risks are visible.

## Pack Version

**Pack Version:** 0.1
**Last Updated:** [YYYY-MM-DD]
**Primary Owner:** [XD Lead]
