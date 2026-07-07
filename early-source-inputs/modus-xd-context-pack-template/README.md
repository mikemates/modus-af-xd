# Experience Design Context Pack Template

This repository contains a reusable Experience Design context pack for Modus delivery teams working in the Modus Agentic Framework.

It is designed to sit beside the Product Context Pack, not replace it. Product Leadership owns business intent, value flow, prioritization, release learning, and adoption tracking. Experience Design extends that shared product spine with the experience structure, sandbox evidence, interaction behavior, content, accessibility, and acceptance context needed by humans and AI agents.

## Quick Start

1. Copy this repository into a new engagement or product initiative.
2. Confirm the design operating mode in `experience-context/00_experience_mode.md`.
3. Complete the minimum required files for the selected mode.
4. Build or link the Experience Sandbox using `experience-sandbox/README.md` and `experience-context/05_sandbox_manifest.md`.
5. Use `11_templates_and_standards/experience_ai_readiness_gate.md` before stories enter implementation.
6. Keep the pack current as decisions, backlog, implementation, and release learning change.

## Relationship to the Product Context Pack

Use the Product Context Pack as the shared product spine:

- business intent
- value flow
- requirements hierarchy
- decision log
- backlog export
- release learning
- adoption scorecard

Use this XD pack as the experience implementation context layer:

- design operating mode
- user roles, jobs, and task context
- journeys and flow logic
- IA, routes, and object model
- Experience Sandbox manifest
- interaction behavior and states
- component and pattern guidance
- content and language guidance
- accessibility and usability expectations
- experience acceptance and QA
- experience measurement

Do not duplicate Product Leadership artifacts. Reference them directly and add the experience detail required for build, review, and agent-assisted delivery.

## Document Structure

```text
README.md
00_README.md
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
  routes.md
  mock_data.md
  handoff_notes.md
  drift_log.md

11_templates_and_standards/
  mode_selection_worksheet.md
  experience_ai_readiness_gate.md
  experience_story_extension.md
  sandbox_review_checklist.md
  experience_qa_checklist.md
  jira_linear_field_mapping.md

agent-instructions/
  AGENTS.md
  prompt_library.md
  review_checklists.md
```

## Core Rules

- Every project must declare a design operating mode.
- The selected mode determines how much Figma, sandbox, research, brand, and system governance are required.
- Mode 1 uses the Experience Sandbox as the primary experience reference unless ambiguity requires Figma.
- The Experience Sandbox is implementation context, not production software.
- Engineering owns production implementation, architecture, code quality, and merge readiness.
- XD owns experience intent, sandbox clarity, UX acceptance, and experience quality review.
- A ticket must not rely on tribal knowledge, Slack threads, or unversioned artifacts.
- Experience-heavy stories must include enough context for an engineer or agent to implement with limited interpretation.
- Interaction behavior, content, accessibility, and instrumentation expectations must be explicit.
- Decisions must be captured in the shared decision log or documented in a linked, versioned file.

## Mode 1 Minimum Context Pack

For the MVP workflow, Mode 1 should use the minimum useful set below:

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

Recommended when workflow language, AI behavior, or user-facing text carries product risk:

```text
experience-context/08_content_language.md
experience-context/13_ai_experience_patterns.md
```

Recommended when product risk remains high or assumptions are not validated:

```text
experience-context/12_research_validation.md
```

## Unknown Markers

Use these markers consistently across the pack:

- **[Assumption]** - Something believed to be true but not validated.
- **[Open question]** - Something unknown that must be answered.
- **[Needs validation]** - A decision or target that must be tested.
- **[Design debt]** - An accepted experience gap that needs later resolution.
- **[Implementation note]** - Guidance for engineering or agents.
- **[Reference only]** - Sandbox code or design material that should guide implementation but not be copied directly.
- **[Reusable candidate]** - Sandbox code, pattern, copy, or behavior that may be reusable in production after engineering review.

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

## Generated For

Modus Experience Design context authoring, Experience Sandbox handoff, AI-ready backlog creation, and experience quality governance.
