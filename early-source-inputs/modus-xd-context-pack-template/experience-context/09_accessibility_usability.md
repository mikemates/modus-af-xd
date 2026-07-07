# 09 - Accessibility and Usability

## Metadata

**Project:** [Project / product name]  
**XD Owner:** [Name]  
**QE Contributor:** [Name]  
**Engineering Contributor:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  

## Purpose

Define accessibility, usability, responsive, compatibility, and readability expectations before build and before release.

Accessibility is part of the design brief, not downstream cleanup. This file defines the minimum experience quality bar and where risk must be accepted or fixed.

## Accessibility Target

**Target standard:** WCAG 2.1 AA / WCAG 2.2 AA / Client standard / Other

**Required by contract or regulation:** Yes / No / Unknown

**Accessibility owner:** [Name]

**Validation owner:** XD / QE / Engineering / External audit

## Accessibility Scope

| Area | Required? | Standard | Owner | Notes |
|---|---:|---|---|---|
| Keyboard navigation | Yes / No | [Standard] | [Owner] | [Notes] |
| Focus management | Yes / No | [Standard] | [Owner] | [Notes] |
| Screen reader semantics | Yes / No | [Standard] | [Owner] | [Notes] |
| Color contrast | Yes / No | [Standard] | [Owner] | [Notes] |
| Form labels and errors | Yes / No | [Standard] | [Owner] | [Notes] |
| Responsive layout | Yes / No | [Standard] | [Owner] | [Notes] |
| Reduced motion | Yes / No | [Standard] | [Owner] | [Notes] |

## Keyboard Navigation Expectations

| Component / flow | Keyboard expectation | Focus order | Escape / cancel behavior | Notes |
|---|---|---|---|---|
| [Component/flow] | [Keys and behavior] | [Order] | [Behavior] | [Notes] |

## Focus Management

| Interaction | Initial focus | Focus after action | Focus after error | Notes |
|---|---|---|---|---|
| [Interaction] | [Target] | [Target] | [Target] | [Notes] |

## Screen Reader Expectations

| Component / state | Semantic requirement | Announcement | Notes |
|---|---|---|---|
| [Component/state] | [Requirement] | [Announcement] | [Notes] |

## Color and Contrast

| Element | Contrast requirement | Current status | Notes |
|---|---|---|---|
| [Element] | [Requirement] | Pass / Fail / Not checked | [Notes] |

## Usability Requirements

| Requirement | Why it matters | Evidence / test method | Owner |
|---|---|---|---|
| [Requirement] | [Reason] | [Evidence] | [Owner] |

## Usability Risks

| Risk | Affected users | Impact | Mitigation | Validation method |
|---|---|---|---|---|
| [Risk] | [Users] | [Impact] | [Mitigation] | [Method] |

## Responsive Requirements

| Breakpoint / device | Layout expectation | Interaction impact | Required for launch? |
|---|---|---|---:|
| Desktop | [Expectation] | [Impact] | Yes / No |
| Tablet | [Expectation] | [Impact] | Yes / No |
| Mobile | [Expectation] | [Impact] | Yes / No |

## Browser and Device Support

| Browser/device | Required? | Notes |
|---|---:|---|
| Chrome | Yes / No | [Notes] |
| Safari | Yes / No | [Notes] |
| Edge | Yes / No | [Notes] |
| Firefox | Yes / No | [Notes] |
| iOS Safari | Yes / No | [Notes] |
| Android Chrome | Yes / No | [Notes] |

## Performance and Perceived Performance

| Experience area | Expectation | Measurement | Notes |
|---|---|---|---|
| Page load | [Expectation] | [Metric] | [Notes] |
| Search/filter | [Expectation] | [Metric] | [Notes] |
| Form submit | [Expectation] | [Metric] | [Notes] |

## Usability Validation Plan

| Question | Method | Participants | Timing | Decision criteria |
|---|---|---|---|---|
| [Question] | [Method] | [Participants] | [Timing] | [Criteria] |

## Accessibility and Usability Debt

| Debt item | Impact | Risk accepted by | Follow-up | Due |
|---|---|---|---|---|
| [Debt] | [Impact] | [Name] | [Story/link] | [Date] |

## Agent Guidance

- Do not rely on color alone to convey status.
- Include keyboard and focus behavior in acceptance criteria when relevant.
- Do not generate inaccessible controls if an accessible component exists.
- If accessibility behavior is undefined, mark it as an open question before implementation.

## Quality Standard

This file is ready when accessibility, usability, responsive, and compatibility expectations are explicit enough to inform backlog acceptance criteria and QE validation.

## Related Documents

- Interaction States: `06_interaction_states.md`
- Components and Patterns: `07_components_patterns.md`
- Experience Acceptance: `10_experience_acceptance.md`
- QE Test Strategy: [Link]
