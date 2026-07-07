# 13 - AI Experience Patterns

## Metadata

**Project:** [Project / product name]  
**XD Owner:** [Name]  
**Product Owner:** [Name]  
**AI / Engineering Contributor:** [Name]  
**QE Contributor:** [Name]  
**Status:** Not Applicable / Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  

## Purpose

Define user-facing AI behavior, trust patterns, human control, uncertainty handling, review states, error recovery, and safety expectations.

Use this file when the product includes AI features that users interact with directly or rely on for decisions, generated content, recommendations, classification, summarization, or workflow automation.

Do not use this file when AI is only used internally by the delivery team.

## AI Feature Summary

| AI capability | User role | Product purpose | User control level | Risk level |
|---|---|---|---|---|
| [Capability] | [Role] | [Purpose] | Suggest / draft / automate / decide | Low / Med / High |

## AI Interaction Principles

### Principle 1: User remains in control

**Meaning:** [Define what control means in this product]

**Implications:**
- [Implication]
- [Implication]

### Principle 2: Uncertainty is visible when it matters

[Repeat structure]

### Principle 3: AI output is reviewable and recoverable

[Repeat structure]

## User Control Model

| AI behavior | User can preview | User can edit | User can reject | User can undo | Required? |
|---|---:|---:|---:|---:|---:|
| [Behavior] | Yes / No | Yes / No | Yes / No | Yes / No | Yes / No |

## Human-in-the-Loop Moments

| Moment | Why human review is needed | Required role | Decision | Audit need |
|---|---|---|---|---|
| [Moment] | [Reason] | [Role] | [Decision] | [Audit] |

## Confidence and Uncertainty Handling

| AI output | Confidence shown? | Threshold | User-facing treatment | Escalation |
|---|---:|---|---|---|
| [Output] | Yes / No | [Threshold] | [Treatment] | [Escalation] |

## Generated Content Editing

| Content type | Editable? | Required review before use? | Version history needed? | Notes |
|---|---:|---:|---:|---|
| [Content] | Yes / No | Yes / No | Yes / No | [Notes] |

## Explainability Requirements

| AI behavior | Explanation needed? | Explanation format | User action supported |
|---|---:|---|---|
| [Behavior] | Yes / No | [Why / sources / confidence / factors] | [Action] |

## Error Recovery

| AI failure mode | User-facing message | Recovery path | Owner |
|---|---|---|---|
| [Failure] | [Copy] | [Recovery] | [Owner] |

## Trust and Transparency Rules

| Rule | Reason | Implementation note |
|---|---|---|
| [Rule] | [Reason] | [Note] |

## Prohibited AI Behaviors

| Prohibited behavior | Reason | Safer alternative |
|---|---|---|
| [Behavior] | [Reason] | [Alternative] |

## Audit and Review Trail

| Event | What must be logged | Who can view | Retention note |
|---|---|---|---|
| [Event] | [Data] | [Role] | [Note] |

## Measurement and Evaluation

| AI behavior | Success signal | Failure signal | Evaluation method |
|---|---|---|---|
| [Behavior] | [Signal] | [Signal] | [Method] |

## Agent Guidance

- Do not create AI experiences that remove required user review.
- Do not present generated content as verified unless the product supports verification.
- Do not hide uncertainty when user decisions depend on it.
- Use explicit review, edit, reject, and undo states where appropriate.
- Escalate high-risk AI behaviors to Product, XD, Engineering, and QE.

## Quality Standard

This file is ready when AI behavior is clear enough to design, implement, test, explain, recover from, and measure without relying on hidden judgment.

## Related Documents

- Experience Intent: `01_experience_intent.md`
- Interaction States: `06_interaction_states.md`
- Content and Language: `08_content_language.md`
- Experience Measurement: `11_experience_measurement.md`
