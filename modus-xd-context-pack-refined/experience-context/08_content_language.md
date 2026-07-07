# 08 - Content and Language

## Metadata

**Project:** [Project / product name]  
**XD / Content Owner:** [Name]  
**Product Owner:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  

## Purpose

Define product terminology, labels, messages, tone, and content rules that guide implementation.

This file prevents agents and teams from inventing product language, using inconsistent labels, or shipping unclear workflow copy.

**Inherits Modus Experience Standards.** Default voice, error-message structure, and button conventions come from the Modus Experience Standards. Capture only this product's terminology, labels, and copy here.

## Content Summary

[2-4 sentences describing the product language strategy.]

Example:

> Product language should be operational, direct, and task-oriented. Labels should match the terms users already use in their workflow. Error messages should explain what happened, what the user can do next, and whether data was saved.

## Voice and Tone

| Context | Tone | Reason | Example |
|---|---|---|---|
| Navigation | [Tone] | [Reason] | [Example] |
| Forms | [Tone] | [Reason] | [Example] |
| Errors | [Tone] | [Reason] | [Example] |
| Empty states | [Tone] | [Reason] | [Example] |
| AI-generated content | [Tone] | [Reason] | [Example] |

## Terminology Glossary

| Concept | Approved term | Avoid | Definition | Notes |
|---|---|---|---|---|
| [Concept] | [Term] | [Term] | [Definition] | [Notes] |

## Navigation Labels

| Route / area | Approved label | Avoid | Notes |
|---|---|---|---|
| [Route] | [Label] | [Avoid] | [Notes] |

## Button and Action Conventions

| Action type | Pattern | Example | Notes |
|---|---|---|---|
| Primary action | Verb + object | [Example] | [Notes] |
| Secondary action | [Pattern] | [Example] | [Notes] |
| Destructive action | [Pattern] | [Example] | [Notes] |
| Cancel action | [Pattern] | [Example] | [Notes] |

## Status Labels

| System state | User-facing label | Definition | Color/icon dependence? | Notes |
|---|---|---|---|---|
| [State] | [Label] | [Definition] | Do not rely only on color / icon | [Notes] |

## Error Message Style

Error messages should answer:

1. What happened?
2. Why did it happen, if useful?
3. What can the user do next?
4. Was data saved or lost?

| Error | Message | Recovery action | Notes |
|---|---|---|---|
| [Error] | [Exact or draft copy] | [Action] | [Notes] |

## Empty State Guidance

| Empty state | Message | Primary action | Secondary action | Notes |
|---|---|---|---|---|
| [State] | [Copy] | [Action] | [Action] | [Notes] |

## Helper Text and Field Guidance

| Field / control | Helper text | Validation message | Notes |
|---|---|---|---|
| [Field] | [Copy] | [Copy] | [Notes] |

## AI-Generated Copy Rules

Use this section only when the product includes user-facing AI content.

| Rule | Reason | Example |
|---|---|---|
| AI output must be editable before submission | User remains accountable | [Example] |
| AI uncertainty must be visible when confidence is low | Avoid false certainty | [Example] |
| Generated content must not be represented as verified unless reviewed | Trust and safety | [Example] |

## Banned or Restricted Phrases

| Phrase | Reason | Replacement |
|---|---|---|
| [Phrase] | [Reason] | [Replacement] |

## Reading Level and Localization

**Target reading level:** [Grade level or standard]

**Localization required:** Yes / No / Future

**Units, dates, currencies:** [Rules]

**Plain language rules:**
- [Rule]
- [Rule]

## Copy Inventory

| Location | Copy | Status | Owner | Story / sandbox link |
|---|---|---|---|---|
| [Route/component] | [Copy] | Draft / Approved / Placeholder | [Owner] | [Link] |

## Agent Guidance

- Use approved terminology and labels from this file.
- Do not invent error messages, empty states, navigation labels, or AI-generated copy rules.
- If exact copy is missing and implementation depends on it, mark it as an open question.
- Copy in acceptance criteria, sandbox, and production should match unless a decision log entry changes it.

## Quality Standard

This file is ready when all implementation-sensitive labels, messages, states, and terminology are defined or explicitly marked as draft/open.

## Related Documents

- IA and Object Model: `04_ia_object_model.md`
- Interaction States: `06_interaction_states.md`
- AI Experience Patterns: `13_ai_experience_patterns.md`
