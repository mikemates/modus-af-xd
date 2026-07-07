# Mock Data

## Purpose

Document the mock or demo data used in the Experience Sandbox so engineering, QE, Product, XD, and agents understand what scenarios are represented.

## Data Principles

- Use representative data, not perfect happy-path-only data.
- Include edge cases that affect layout, validation, status, or decision-making.
- Do not include real client-confidential or regulated data unless approved.
- Mark fake data clearly.
- Align object names with `../experience-context/04_ia_object_model.md`.

## Data Sets

| Data set | File / location | Purpose | Objects represented | Edge cases included |
|---|---|---|---|---|
| [Data set] | [Path] | [Purpose] | [Objects] | [Edge cases] |

## Scenario Coverage

| Scenario | Data needed | Included? | Notes |
|---|---|---:|---|
| Happy path | [Data] | Yes / No | [Notes] |
| Empty state | [Data] | Yes / No | [Notes] |
| Error state | [Data] | Yes / No | [Notes] |
| Permission state | [Data] | Yes / No | [Notes] |
| Large list / stress case | [Data] | Yes / No | [Notes] |

## Object Examples

### [Object Name]

```json
{
  "id": "example-id",
  "status": "example-status",
  "name": "Example Name"
}
```

## Data Gaps

| Gap | Impact | Needed before backlog? | Owner |
|---|---|---:|---|
| [Gap] | [Impact] | Yes / No | [Owner] |
