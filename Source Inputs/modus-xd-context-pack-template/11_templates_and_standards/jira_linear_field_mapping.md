# Jira / Linear Field Mapping for Experience Context

Use this mapping to add experience context to backlog tools without duplicating the full context pack inside every ticket.

## Recommended Fields

| Field | Type | Required when | Source |
|---|---|---|---|
| Design Mode | Select | All experience-heavy work | `00_experience_mode.md` |
| Experience Reference URL | URL | Visual/interaction work | Sandbox/Figma/context link |
| Sandbox Route | Text/URL | Mode 1 or sandbox-supported Mode 2 | `05_sandbox_manifest.md` |
| Flow ID | Text | Flow-based work | `03_journeys_flows.md` |
| Route ID | Text | Screen/route work | `04_ia_object_model.md` |
| UX Acceptance Criteria | Long text | Experience-heavy stories | `10_experience_acceptance.md` |
| Accessibility Requirement | Long text | All visual/interaction work | `09_accessibility_usability.md` |
| Content Source | URL/text | Copy-sensitive work | `08_content_language.md` |
| Instrumentation Events | Long text | Behavior-change work | `11_experience_measurement.md` |
| Measurement Hypothesis | Long text | Feature/epic/story with expected behavior change | `11_experience_measurement.md` |
| Experience QA Status | Select | Before release/demo | `experience_qa_checklist.md` |
| Design Debt | Long text | When experience gap is accepted | `10_experience_acceptance.md` |

## Example Jira Story Fields

```text
Design Mode: Mode 1
Experience Reference URL: [sandbox route URL]
Sandbox Route: /quotes/review/:id
Flow ID: F-003 Quote Review
Route ID: R-006 Quote Detail Review
Content Source: experience-context/08_content_language.md#quote-review
Accessibility Requirement: Keyboard path through table, filter panel, and submit action required.
Instrumentation Events: quote_review_started, quote_review_submitted, quote_review_error
Experience QA Status: Not reviewed
Design Debt: None
```

## Field Use Rules

- Use links to canonical files rather than duplicating large sections.
- Include exact copy in the ticket only when implementation depends on it.
- Include exact ACs in the ticket.
- Do not rely on "see prototype" as the only instruction.
- If the experience reference is stale, the story is not ready.

## Status Values

### Experience QA Status

- Not reviewed
- Needs changes
- Accepted with debt
- Accepted
- Blocked

### Design Debt Status

- None
- Proposed
- Accepted
- Follow-up created
- Resolved

## Import Notes

For tools that do not support custom fields, add the `experience_story_extension.md` content to the story description.
