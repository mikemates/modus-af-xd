# Experience QA Checklist

Use this checklist during sprint reviews, demos, release readiness, and pre-handoff QA.

## QA Metadata

**Project:** [Name]

**Build / environment:** [URL]

**Review date:** [YYYY-MM-DD]

**Reviewer(s):** [Names]

**Related sandbox version:** [Branch/tag/commit]

**Outcome:** Pass / Pass with debt / Fail

## Critical Flow Review

| Flow | Expected outcome | Status | Notes |
|---|---|---|---|
| [Flow] | [Outcome] | Pass / Fail / N/A | [Notes] |

## IA and Navigation

- [ ] Navigation labels match approved terminology.
- [ ] Route/page structure matches the accepted IA or documented decision changes.
- [ ] Users can identify where they are.
- [ ] Users can identify the next appropriate action.
- [ ] Role/permission visibility behaves as expected.

## Interaction Behavior

- [ ] Default states behave as expected.
- [ ] Loading states behave as expected.
- [ ] Empty states behave as expected.
- [ ] Error states behave as expected.
- [ ] Success and confirmation states behave as expected.
- [ ] Validation messages are clear and triggered appropriately.
- [ ] Undo/cancel/retry behavior works where required.

## Components and Visual Coherence

- [ ] Approved components are used.
- [ ] Component variants/states are correct.
- [ ] Layout is consistent with approved patterns.
- [ ] Visual hierarchy supports the task.
- [ ] Known deviations are documented.

## Content

- [ ] Labels match approved terms.
- [ ] Error messages are clear and actionable.
- [ ] Empty states explain what happened and what to do next.
- [ ] Button/action language is consistent.
- [ ] Placeholder copy has been removed or accepted as debt.

## Accessibility and Usability

- [ ] Required keyboard paths work.
- [ ] Focus order is logical.
- [ ] Focus is managed after modals, errors, and submissions.
- [ ] Screen reader semantics are acceptable for required components.
- [ ] Contrast/status does not rely on color alone.
- [ ] Required responsive breakpoints work.

## Measurement

- [ ] Required events are implemented.
- [ ] Event triggers match the measurement plan.
- [ ] Event properties are present.
- [ ] Friction signals can be observed.

## Findings Log

| Finding ID | Area | Severity | Finding | Recommendation | Status |
|---|---|---|---|---|---|
| XDQA-001 | [Area] | Low / Med / High / Blocker | [Finding] | [Recommendation] | Open / Closed / Accepted |

## Launch Blockers

| Blocker | Required fix | Owner | Status |
|---|---|---|---|
| [Blocker] | [Fix] | [Owner] | Open / Fixed |

## Accepted Debt

| Debt item | Risk | Accepted by | Follow-up |
|---|---|---|---|
| [Debt] | [Risk] | [Name] | [Story/link] |

## Final QA Decision

**Decision:** Pass / Pass with debt / Fail

**Rationale:** [Reason]

**Required follow-up:**
- [Item]
- [Item]
