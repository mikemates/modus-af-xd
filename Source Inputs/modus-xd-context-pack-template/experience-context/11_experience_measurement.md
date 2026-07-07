# 11 - Experience Measurement

## Metadata

**Project:** [Project / product name]  
**XD Owner:** [Name]  
**Product Owner:** [Name]  
**Data / Analytics Owner:** [Name]  
**Engineering Contributor:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  
**Related Adoption Scorecard:** [Link to Product Context Pack `07_adoption_scorecard.md`]  

## Purpose

Define how the team will measure whether the experience is helping users complete work, reduce friction, adopt the product, and realize value.

Product Leadership owns adoption and business outcomes. XD contributes task success, friction, comprehension, time-to-value, error recovery, and behavior signals.

## Measurement Summary

[2-4 sentences describing what the team needs to learn from usage and why.]

## Experience Measurement Hypothesis

> If we [experience change], then [target behavior] will improve, because [reason]. We will know this is working when [leading signal] improves and [friction signal] decreases.

| Hypothesis element | Definition |
|---|---|
| Experience change | [What changes in the product] |
| Target behavior | [What users should do differently] |
| Product outcome | [Related product/business outcome] |
| Leading indicator | [Early signal] |
| Friction indicator | [Confusion/error/abandonment/delay signal] |
| Lagging indicator | [Adoption/business outcome] |
| Baseline needed | [What we need to know before launch] |
| Instrumentation needed | [Events/properties/evidence] |
| Review cadence | [Weekly/monthly/release-based] |

## Task Success Metrics

| Task | Success metric | Baseline | Target | Instrumentation | Owner |
|---|---|---|---|---|---|
| [Task] | [Metric] | [Baseline] | [Target] | [Event/property] | [Owner] |

## Friction Signals

| Friction signal | What it may mean | Where measured | Action if triggered |
|---|---|---|---|
| Abandonment | [Meaning] | [Flow/event] | [Action] |
| Repeated validation errors | [Meaning] | [Form/event] | [Action] |
| Backtracking | [Meaning] | [Route/event] | [Action] |
| Support/contact spike | [Meaning] | [Source] | [Action] |
| Long completion time | [Meaning] | [Flow/event] | [Action] |

## Instrumentation Plan

| Event name | Trigger | Properties | Related flow/story | Owner | Status |
|---|---|---|---|---|---|
| [event_name] | [Trigger] | [Properties] | [Flow/story] | [Owner] | Planned / Implemented / Verified |

## Event Naming Guidance

Use clear event names that describe user behavior.

Recommended pattern:

```text
object_action_result
```

Examples:

```text
quote_review_started
quote_review_submitted
document_upload_failed
exception_filter_applied
ai_suggestion_accepted
ai_suggestion_edited
```

## Baseline Plan

| Baseline needed | Source | Owner | Due | Notes |
|---|---|---|---|---|
| [Baseline] | [Analytics/research/support/manual observation] | [Owner] | [Date] | [Notes] |

## Qualitative Learning Signals

| Question | Method | Source | Cadence | Owner |
|---|---|---|---|---|
| [Question] | User test / interview / support review / session replay | [Source] | [Cadence] | [Owner] |

## Adoption Scorecard Integration

| Product adoption metric | Experience signal that contributes | Evidence | Notes |
|---|---|---|---|
| [Metric from PL scorecard] | [Experience signal] | [Source] | [Notes] |

## Review Cadence

| Review | Participants | Cadence | Decisions made |
|---|---|---|---|
| Flow performance review | Product + XD + Data | [Cadence] | [Decisions] |
| Release learning review | Product + XD + Engineering + QE | [Cadence] | [Decisions] |
| Adoption review | Product + Data + XD | [Cadence] | [Decisions] |

## Measurement Risks

| Risk | Impact | Mitigation | Owner |
|---|---|---|---|
| [Risk] | [Impact] | [Mitigation] | [Owner] |

## Agent Guidance

- Do not generate analytics events that conflict with this file.
- Add instrumentation expectations to experience-heavy stories.
- If a story changes user behavior, check whether a metric or event is needed.
- If measurement is not possible, document the proxy signal.

## Quality Standard

This file is ready when each major flow has a defined success signal, friction signal, instrumentation need, baseline plan, and review cadence.

## Related Documents

- Product Adoption Scorecard: [Link]
- Experience Intent: `01_experience_intent.md`
- Journeys and Flows: `03_journeys_flows.md`
- Backlog Field Mapping: `../11_templates_and_standards/jira_linear_field_mapping.md`
