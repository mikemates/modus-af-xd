# 10 - Experience Acceptance

## Metadata

**Project:** [Project / product name]  
**XD Owner:** [Name]  
**Product Owner:** [Name]  
**Engineering Lead:** [Name]  
**QE Lead:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  

## Purpose

Define what "good enough" means for the product experience before demo, launch, or handoff.

This file gives the team a shared standard for UX acceptance, design QA, accessibility checks, acceptable debt, and launch blockers.

## Acceptance Summary

[2-4 sentences summarizing the experience quality bar.]

Example:

> The release is acceptable when the core workflow can be completed end to end by the primary role, critical states are handled, terminology is consistent, accessibility blockers are resolved or risk-accepted, and known experience debt is documented with follow-up ownership.

## Experience Acceptance Gates

| Gate | Timing | Required evidence | Owner | Status |
|---|---|---|---|---|
| Experience direction | Before sandbox build | Intent, users, flows, IA | XD + Product | Draft / Ready |
| Sandbox readiness | Before backlog handoff | Sandbox manifest and review notes | XD + Engineering | Draft / Ready |
| AI-ready backlog | Before implementation | Story extension and readiness gate | Product + XD + Engineering + QE | Draft / Ready |
| Experience QA | Before demo/release | QA checklist and issue log | XD + QE | Draft / Ready |
| Launch acceptance | Before launch/handoff | Blockers resolved or debt accepted | Product + XD + QE + Engineering | Draft / Ready |

## UX Acceptance Criteria

Use these for flow-level or story-level UX acceptance.

| AC ID | Flow / story | UX acceptance criterion | Evidence | Owner |
|---|---|---|---|---|
| UX-AC-001 | [Flow/story] | [Criterion] | [Sandbox/test/build review] | [Owner] |

## Flow Completion Checks

| Flow | Primary role | Completion criteria | Status | Notes |
|---|---|---|---|---|
| [Flow] | [Role] | [What must work] | Pass / Fail / Risk accepted | [Notes] |

## Design QA Checklist

| Area | Check | Required for launch? | Status | Notes |
|---|---|---:|---|---|
| Flow | Critical flows work end to end | Yes / No | Pass / Fail / N/A | [Notes] |
| IA | Navigation labels and route structure match intent | Yes / No | Pass / Fail / N/A | [Notes] |
| Components | Approved components/patterns are used | Yes / No | Pass / Fail / N/A | [Notes] |
| States | Empty/loading/error/success states are handled | Yes / No | Pass / Fail / N/A | [Notes] |
| Content | Labels, messages, and helper text are clear | Yes / No | Pass / Fail / N/A | [Notes] |
| Accessibility | Accessibility expectations are met or risk-accepted | Yes / No | Pass / Fail / N/A | [Notes] |
| Responsive | Required breakpoints work | Yes / No | Pass / Fail / N/A | [Notes] |
| Measurement | Required events/instrumentation are present | Yes / No | Pass / Fail / N/A | [Notes] |

## Launch Blockers

A launch blocker is an issue that materially prevents task completion, creates serious confusion, violates required accessibility expectations, breaks a critical flow, or undermines product trust.

| Blocker | Impact | Required fix | Owner | Status |
|---|---|---|---|---|
| [Blocker] | [Impact] | [Fix] | [Owner] | Open / Fixed / Risk accepted |

## Acceptable Experience Debt

Debt is acceptable only when the team names it, understands the risk, and creates a follow-up path.

| Debt item | Why acceptable now | Risk | Follow-up | Owner | Due |
|---|---|---|---|---|---|
| [Debt] | [Reason] | [Risk] | [Story/link] | [Owner] | [Date] |

## Experience QA Findings

| Finding ID | Date | Area | Severity | Finding | Recommendation | Status |
|---|---|---|---|---|---|---|
| XDQA-001 | [Date] | [Area] | Low / Med / High / Blocker | [Finding] | [Recommendation] | Open / Closed / Accepted |

## Signoff Model

| Signoff | Owner | Evidence | Status |
|---|---|---|---|
| Product outcome alignment | [Name] | [Evidence] | Pending / Approved |
| Experience acceptance | [Name] | [Evidence] | Pending / Approved |
| Technical readiness | [Name] | [Evidence] | Pending / Approved |
| QE/release readiness | [Name] | [Evidence] | Pending / Approved |
| Accessibility risk acceptance | [Name] | [Evidence] | Pending / Approved / N/A |

## Agent Guidance

- Use this file to determine whether a story or release meets experience expectations.
- Do not downgrade launch blockers to debt without an explicit risk acceptance decision.
- If acceptance evidence is missing, mark the story or release as not ready.

## Quality Standard

This file is ready when the team can make a confident go/no-go decision on experience quality without relying on subjective opinions or undocumented judgment.

## Related Documents

- Experience Intent: `01_experience_intent.md`
- Sandbox Manifest: `05_sandbox_manifest.md`
- Interaction States: `06_interaction_states.md`
- Accessibility and Usability: `09_accessibility_usability.md`
- QE Test Plan: [Link]
