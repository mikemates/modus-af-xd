# Experience Design Context Pack Template

A reusable Experience Design context pack for Modus delivery teams working in the Modus Agentic Framework. It captures the experience structure, sandbox evidence, interaction behavior, content, accessibility, and acceptance context that humans and AI agents need to build the right product.

It is designed to sit beside the Product Context Pack, not replace it. Product Leadership owns business intent, value flow, prioritization, release learning, and adoption tracking. XD extends that shared product spine with the experience implementation layer. For the mechanics of wiring the two together, see `PL_INTEGRATION.md`.

**New to the pack?** Read `GETTING_STARTED.md` first — it walks through how to populate the folder step by step. This README is the reference (file list, purposes, mode table).

**Two things this pack leans on that live outside it:** the *Modus Experience Standards* (the house defaults for accessibility, interaction states, responsiveness, content, and components — this pack records only per-product deltas), and the *Intake Workflow* (`agent-instructions/intake_workflow.md`) for turning raw transcripts/research/artifacts into drafted context files.

## Quick Start

1. Copy this repository into a new engagement or product initiative.
2. Confirm the design operating mode in `experience-context/00_experience_mode.md`.
3. Complete the minimum required files for the selected mode (see Required Files by Mode).
4. Build or link the Experience Sandbox using `experience-sandbox/README.md` and `experience-context/05_sandbox_manifest.md`.
5. Use `templates-and-standards/experience_ai_readiness_gate.md` before stories enter implementation.
6. Keep the pack current as decisions, backlog, implementation, and release learning change.

## Relationship to the Product Context Pack

Use the Product Context Pack as the shared product spine (business intent, value flow, requirements hierarchy, decision log, backlog export, release learning, adoption scorecard). Use this XD pack as the experience implementation context layer (design mode, users/roles, journeys/flows, IA/object model, sandbox manifest, interaction behavior, components, content, accessibility, acceptance, measurement).

Do not duplicate Product Leadership artifacts. Reference them directly and add the experience detail required for build, review, and agent-assisted delivery. `PL_INTEGRATION.md` maps each Product Context Pack file to its XD contribution and defines the non-duplication rules, shared decision log, and backlog standard.

## Document Structure

```text
README.md
GETTING_STARTED.md
PL_INTEGRATION.md

experience-context/
  00_experience_mode.md
  01_experience_intent.md
  02_users_tasks_roles.md
  03_journeys_flows.md
  04_ia_object_model.md
  05_sandbox_manifest.md
  06_interaction_states.md
  07_components_patterns.md
  08_content_language.md
  09_accessibility_usability.md
  10_experience_acceptance.md
  11_experience_measurement.md
  12_research_validation.md
  13_ai_experience_patterns.md

experience-sandbox/
  README.md
  drift_log.md

templates-and-standards/
  mode_selection_worksheet.md
  experience_ai_readiness_gate.md
  experience_story_extension.md
  experience_quality_review.md
  jira_linear_field_mapping.md

agent-instructions/
  AGENTS.md
  prompt_library.md
  intake_workflow.md
```

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
    -> templates-and-standards/experience_ai_readiness_gate.md
    -> templates-and-standards/experience_quality_review.md
    -> experience-sandbox/drift_log.md
```

## Document Purposes

### Operating Model

**00_experience_mode.md** — Which design mode applies, why it fits this product, the role of Figma/sandbox/research/brand/design-system governance, and which artifacts are required or intentionally omitted.

### Experience Direction

**01_experience_intent.md** — What user behavior must change, what the experience should make easier/faster/clearer/safer, and what must not drift during implementation.

**02_users_tasks_roles.md** — Who uses the product; the jobs and tasks that matter; the roles, permissions, expertise levels, and contexts of use that affect design.

**03_journeys_flows.md** — Hero flows, secondary flows, edge cases, handoffs, failure paths, and which flows the sandbox covers.

**04_ia_object_model.md** — How the product is organized: routes, objects, relationships, terminology, filters, and visibility rules.

### Sandbox and Build Context

**05_sandbox_manifest.md** — What the Experience Sandbox includes; which routes, states, flows, and stories it represents; and what is reusable, reference-only, or intentionally divergent from production.

**06_interaction_states.md** — How the product behaves across states, validation, errors, permissions, confirmations, keyboard use, and edge cases.

**07_components_patterns.md** — The component library or design system in use, and which components and patterns are approved, adapted, missing, or debt.

**08_content_language.md** — Terms, labels, button conventions, error copy, empty states, and tone rules.

### Quality and Learning

**09_accessibility_usability.md** — Accessibility, usability, responsive, compatibility, and readability expectations.

**10_experience_acceptance.md** — What makes the experience acceptable before demo, release, or handoff, and what blocks launch versus becomes accepted debt.

**11_experience_measurement.md** — The behavior, friction, adoption, and task-success signals that show whether the experience is working.

**12_research_validation.md** — Assumptions that need research or validation, and the evidence required before build, release, or scale.

**13_ai_experience_patterns.md** — User-facing AI rules, including human control, uncertainty, editing, auditability, and trust.

## Required Files by Mode

| File | Mode 0 | Mode 1 | Mode 2 | Mode 3 |
|---|---|---|---|---|
| 00_experience_mode | Required | Required | Required | Required |
| 01_experience_intent | Required | Required | Required | Required |
| 02_users_tasks_roles | Required | Required | Required | Required |
| 03_journeys_flows | Required | Required | Required | Required |
| 04_ia_object_model | Light | Light | Required | Required |
| 05_sandbox_manifest | Optional | Required if sandbox used | Required if sandbox used | Optional/supporting |
| 06_interaction_states | Light | Required | Required | Required |
| 07_components_patterns | Optional | Recommended | Required | Required |
| 08_content_language | Optional | Light | Recommended | Required |
| 09_accessibility_usability | Required | Required | Required | Required |
| 10_experience_acceptance | Optional | Required | Required | Required |
| 11_experience_measurement | Recommended | Required | Required | Required |
| 12_research_validation | Required | Recommended | Recommended | Recommended |
| 13_ai_experience_patterns | If relevant | If relevant | If relevant | If relevant |

Mode 1 is code-first and deliberately lighter than Mode 3: in Mode 1 the sandbox demonstrates IA, components, and content, so those files stay Light/Recommended rather than Required. Mode 3 is Figma- and design-system-governed, so the same files become Required. "Light" means capture only what the sandbox does not already make obvious.

### Mode 1 Minimum Context Pack

For the MVP workflow, start with the minimum useful set and add the rest only when the work calls for it:

```text
experience-context/00_experience_mode.md
experience-context/01_experience_intent.md
experience-context/02_users_tasks_roles.md
experience-context/03_journeys_flows.md
experience-context/04_ia_object_model.md
experience-context/05_sandbox_manifest.md
experience-context/06_interaction_states.md
experience-context/07_components_patterns.md
experience-context/09_accessibility_usability.md
experience-context/10_experience_acceptance.md
experience-context/11_experience_measurement.md
```

Add `08_content_language.md` and `13_ai_experience_patterns.md` when workflow language, AI behavior, or user-facing text carries product risk. Add `12_research_validation.md` when product risk remains high or assumptions are not validated.

## Core Rules

- Every project must declare a design operating mode; the mode determines how much Figma, sandbox, research, brand, and system governance are required.
- Mode 1 uses the Experience Sandbox as the primary experience reference unless ambiguity requires Figma.
- The Experience Sandbox is implementation context, not production software.
- Engineering owns production implementation, architecture, code quality, and merge readiness. XD owns experience intent, sandbox clarity, UX acceptance, and experience quality review.
- A ticket must not rely on tribal knowledge, Slack threads, or unversioned artifacts. Experience-heavy stories must include enough context for an engineer or agent to implement with limited interpretation.
- Interaction behavior, content, accessibility, and instrumentation expectations must be explicit.
- Decisions must be captured in the shared decision log or a linked, versioned file.

## Unknown Markers

Use these markers consistently across the pack:

- **[Assumption]** — Believed true but not validated.
- **[Open question]** — Unknown that must be answered.
- **[Needs validation]** — A decision or target that must be tested.
- **[Design debt]** — An accepted experience gap that needs later resolution.
- **[Implementation note]** — Guidance for engineering or agents.
- **[Reference only]** — Sandbox code or design material that should guide implementation but not be copied directly.
- **[Reusable candidate]** — Sandbox code, pattern, copy, or behavior that may be reusable in production after engineering review.

## Using This Pack by Role

**Experience Design** — Own the experience-context files and the sandbox manifest. Define interaction behavior, content, accessibility, and UX acceptance. Review built software against experience intent.

**Product Leadership** — Own the Product Context Pack. Keep business intent, value flow, prioritization, release learning, and adoption current. Partner with XD on experience intent, measurement hypotheses, and AI-ready backlog.

**Engineering** — Use the sandbox and context files as implementation input. Decide what sandbox code is reusable vs. reference-only. Own production architecture, code quality, standards, and merge readiness.

**QE** — Use the pack to design functional, regression, accessibility, and release validation. Review acceptance criteria for testability. Partner with XD on experience QA and release readiness.

**AI Agents** — Read `agent-instructions/AGENTS.md` before acting. Treat context files, the sandbox manifest, linked stories, and approved decisions as canonical input. Do not invent missing user intent, layout, state behavior, copy, permissions, accessibility rules, or measurement events.

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

## Maintenance

| Task | Frequency | Owner |
|---|---|---|
| Review mode and required artifacts | Project start and major scope changes | XD Lead + Product Lead |
| Update sandbox manifest | After sandbox changes or backlog refinement | XD Lead |
| Update interaction states | Before AI-ready backlog review | XD Lead |
| Update accessibility/usability guidance | Before build and before release | XD Lead + QE |
| Update experience measurement | Before implementation and after release | XD Lead + Product/Data |
| Review AI readiness | Before sprint planning or implementation handoff | Product + XD + Engineering + QE |
| Capture sandbox drift | During build and after release | XD Lead + Engineering Lead |

## Pack Version

**Pack Version:** 0.2
**Last Updated:** [YYYY-MM-DD]
**Primary Owner:** [XD Lead]

Generated for Modus Experience Design context authoring, Experience Sandbox handoff, AI-ready backlog creation, and experience quality governance.
