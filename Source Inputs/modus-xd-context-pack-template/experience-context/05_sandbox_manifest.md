# 05 - Experience Sandbox Manifest

## Metadata

**Project:** [Project / product name]  
**Sandbox owner:** [XD owner]  
**Engineering reviewer:** [Engineering lead]  
**Product reviewer:** [Product lead]  
**QE reviewer:** [QE lead]  
**Status:** Draft / In Review / Approved for Backlog / Superseded  
**Last Updated:** [YYYY-MM-DD]  

## Purpose

Map the Experience Sandbox to product intent, flows, routes, states, backlog, decisions, and implementation relevance.

This is the bridge between a design-authored coded experience and production implementation. Without this file, the sandbox can become a prototype that looks useful but is not structured enough for engineering or agents to trust.

## Sandbox Summary

**Sandbox repository:** [URL]

**Sandbox branch / version:** [Branch, tag, commit, or release]

**Local run command:** [Command]

**Preview URL:** [URL]

**Primary design mode:** Mode 1 / Mode 2 / Mode 3 support

**Component library / UI foundation:** [Name]

**Mock data source:** [File or folder]

**Production relationship:** Reference only / Reusable candidates / Shared component experiments / Other

## Sandbox Intent

[2-4 sentences describing what the sandbox demonstrates and why it exists.]

Example:

> This sandbox demonstrates the core intake, review, and exception-resolution workflow for [user role]. It is intended to clarify flow logic, route structure, states, and interaction behavior before engineering implementation. It is not production software and should be treated as implementation context unless engineering explicitly marks code as reusable.

## What the Sandbox Includes

- [Primary flow]
- [Route]
- [State behavior]
- [Object/list/detail pattern]
- [Form/validation behavior]
- [Content pattern]
- [Other]

## What the Sandbox Does Not Include

- [Production API integration]
- [Authentication]
- [Authorization enforcement]
- [Production architecture]
- [Full responsive behavior]
- [Other]

## Route and Flow Coverage

| Route ID | Sandbox route | Page / screen | Related flow | States shown | Backlog link | Status |
|---|---|---|---|---|---|---|
| R-001 | [/route] | [Page] | [Flow ID] | Default, empty, loading, error, success | [Epic/story] | Draft / Ready |

## State Coverage Matrix

| Flow / route | Default | Loading | Empty | Error | Success | Permission state | Notes |
|---|---:|---:|---:|---:|---:|---:|---|
| [Route] | Yes / No | Yes / No | Yes / No | Yes / No | Yes / No | Yes / No | [Notes] |

## Backlog Mapping

| Sandbox element | Related feature | Related epic | Related story | Implementation relevance | Notes |
|---|---|---|---|---|---|
| [Route/component/state] | [Feature] | [Epic] | [Story] | Reference only / Reusable candidate / Needs rebuild | [Notes] |

## Implementation Relevance

Use this section to prevent confusion about what engineering should reuse, reinterpret, or ignore.

### Reusable Candidates

| Sandbox file/component/pattern | Why it may be reusable | Engineering review needed | Status |
|---|---|---|---|
| [Path or component] | [Reason] | [Review need] | Not reviewed / Approved / Rejected |

### Reference-Only Elements

| Sandbox file/component/pattern | Why reference-only | Production implication |
|---|---|---|
| [Path or component] | [Reason] | [How production should handle it] |

### Intentionally Divergent from Production

| Sandbox choice | Why it differs | Production expectation |
|---|---|---|
| [Choice] | [Reason] | [Expectation] |

## Mock Data Coverage

| Data set | Purpose | Objects represented | Edge cases represented | Source file |
|---|---|---|---|---|
| [Data set] | [Purpose] | [Objects] | [Edge cases] | [Path] |

## Component and Pattern Assumptions

| Pattern / component | Sandbox implementation | Production expectation | Open question |
|---|---|---|---|
| [Pattern] | [How shown] | [Expected] | [Question] |

## Content and Terminology Notes

| Text / label / message | Status | Source | Notes |
|---|---|---|---|
| [Copy] | Draft / Approved / Placeholder | [Context file] | [Notes] |

## Accessibility Notes

| Area | Sandbox support | Production expectation | Risk |
|---|---|---|---|
| Keyboard navigation | [Support] | [Expectation] | [Risk] |
| Focus management | [Support] | [Expectation] | [Risk] |
| Screen reader semantics | [Support] | [Expectation] | [Risk] |
| Color contrast | [Support] | [Expectation] | [Risk] |

## Engineering Review Notes

| Date | Reviewer | Finding | Decision / action | Owner |
|---|---|---|---|---|
| [Date] | [Name] | [Finding] | [Action] | [Owner] |

## Sandbox Readiness Checklist

Before the sandbox becomes implementation input:

- [ ] Core flow is represented end to end.
- [ ] Major routes/screens are included.
- [ ] Key states are visible or explicitly documented as missing.
- [ ] Mock/demo data is sufficient to explain intended behavior.
- [ ] Component usage is realistic enough for engineering review.
- [ ] Interaction behavior is clear enough to convert into stories.
- [ ] Content is final enough where implementation depends on it.
- [ ] Accessibility expectations are documented.
- [ ] Engineering has reviewed feasibility.
- [ ] Reference-only versus reusable elements are documented.
- [ ] Open questions are documented.
- [ ] Backlog links are mapped.

## Drift Management

Use `../experience-sandbox/drift_log.md` to capture differences between sandbox and production implementation.

| Drift item | Date found | Impact | Decision | Owner |
|---|---|---|---|---|
| [Drift] | [Date] | [Impact] | [Decision] | [Owner] |

## Agent Guidance

When using the sandbox:

- Treat this manifest as the source of truth for what the sandbox means.
- Do not assume sandbox code is production-ready.
- Do not copy sandbox code marked reference-only.
- Preserve route/state/flow intent unless the backlog or decision log says otherwise.
- Ask for clarification if a sandbox route is not mapped to a flow or story.

## Quality Standard

This file is ready when engineering and agents can identify what the sandbox demonstrates, how it maps to backlog, which states matter, and what code or behavior is reference-only versus potentially reusable.

## Related Documents

- Experience Sandbox README: `../experience-sandbox/README.md`
- Routes: `../experience-sandbox/routes.md`
- Mock Data: `../experience-sandbox/mock_data.md`
- Handoff Notes: `../experience-sandbox/handoff_notes.md`
- Drift Log: `../experience-sandbox/drift_log.md`
- AI Readiness Gate: `../11_templates_and_standards/experience_ai_readiness_gate.md`
