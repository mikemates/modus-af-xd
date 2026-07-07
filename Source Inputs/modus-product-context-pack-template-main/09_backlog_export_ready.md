# Backlog Export Ready

This document formats all requirements for export to Jira, Linear, or similar tools. Use this as your single source of truth for what to create in your execution platform.

**Important:** This is auto-generated from `03_requirement_hierarchy.md`. Do not manually edit here; update the hierarchy document and regenerate this file.

---

## Export Format Guide

- **Jira Field Mapping:** See `11_templates_and_standards/jira_field_mapping.md`
- **Export Instructions:** [Tools and scripts to import these into Jira/Linear]
- **Validation:** [Run these checks before import to catch errors]

---

## Strategic Themes

### Theme 1: [Theme Name]

**Theme ID:** ST-001

**Description:** [Business investment area and strategic importance]

**Status:** Active / Planned / Completed

**Duration:** [Timeline]

**Owner:** [PM/Lead]

---

## Features (Linked to Strategic Themes)

### Feature 1.1: [Feature Name]

**Feature ID:** F-001

**Strategic Theme:** ST-001

**Description:** [Feature description with value hypothesis]

**Value Hypothesis:** 
> "If we [build this feature], then [customer outcome], resulting in [business outcome]."

**Status:** Active / Planned / Completed

**Timeline:** [Start date] - [End date] (6-9 months)

**Owner:** [PM/Engineering Lead]

**Feature KRs:**
| KR ID | KR Statement | Target | Measurement |
|-------|---|---|---|
| F-001.KR1 | [Business outcome] | [Target] | [Metric] |
| F-001.KR2 | [Business outcome] | [Target] | [Metric] |

**[Assumption]** [Critical assumptions about this feature]

**[Open question]** [Unknowns we'll learn about]

---

## Epics (Linked to Features)

### Epic 1.1.1: [Epic Name]

**Epic ID:** E-001

**Parent Feature:** F-001 → Feature KR: F-001.KR1

**Description:** [Epic scope and deliverables]

**Status:** Active / Planned / Not Started

**Timeline:** [Start] - [End] (target: ≤3 months)

**Owner:** [Engineering Lead]

**Epic KRs:**
| KR ID | KR Statement | Target | Measurement |
|-------|---|---|---|
| E-001.KR1 | [Outcome] | [Target] | [Metric] |
| E-001.KR2 | [Outcome] | [Target] | [Metric] |

**Child User Stories:** 
- US-001
- US-002
- US-003

---

## User Stories (Linked to Epics)

### User Story 1: [Story Name]

**User Story ID:** US-001

**Epic:** E-001

**User Story:**
```
As a [user role],
I want to [action/feature],
So that [business value].
```

**Acceptance Criteria:**
- [ ] AC-1: [Observable behavior] [Maps to: E-001.KR1]
- [ ] AC-2: [Observable behavior] [Maps to: E-001.KR1]
- [ ] AC-3: [Observable behavior] [Maps to: E-001.KR2]

**Acceptance Criteria Mapping:**
| AC | Maps to KR | Validation Method |
|---|---|---|
| AC-1 | E-001.KR1 | [How we'll verify] |
| AC-2 | E-001.KR1 | [How we'll verify] |
| AC-3 | E-001.KR2 | [How we'll verify] |

**Status:** Ready / In Progress / Done

**Story Points:** [Estimate]

**Assigned To:** [Engineer]

**Sprint:** [Sprint name or date]

**Dependencies:**
- [Other stories this depends on]
- [Infrastructure/setup needed]

**Definition of Done:**
- [ ] Code reviewed
- [ ] Unit tests pass
- [ ] Acceptance criteria met
- [ ] Product owner sign-off

---

### User Story 2: [Story Name]

**User Story ID:** US-002

[Repeat structure]

---

## Jira/Linear Export Format

### Bulk Upload: Epics

```csv
Epic Name,Epic Key,Epic Summary,Epic Description,Component,Labels,Status
[Epic Name],[Key],[Summary],[Description],[Component],[Labels],Active
```

### Bulk Upload: Features

```csv
Feature Name,Feature Key,Feature Summary,Feature Description,Epic Link,Component,Labels,Status
[Feature Name],[Key],[Summary],[Description],[Epic Key],[Component],[Labels],Active
```

### Bulk Upload: User Stories

```csv
Story Name,Story Key,Story Summary,Story Description,Epic Link,Status,Story Points,Assignee,Sprint
[Story Name],[Key],[Summary],[Description],[Epic Key],Active,[Points],[Assignee],[Sprint]
```

---

## Import Validation Checklist

Before importing into Jira/Linear:

- [ ] All Features have exactly one parent Strategic Theme
- [ ] All Epics have exactly one parent Feature and map to one Feature KR
- [ ] All User Stories have exactly one parent Epic
- [ ] All Acceptance Criteria map to at least one Epic KR
- [ ] All Status values are valid (Active / Planned / Not Started / Done)
- [ ] All required fields are populated (Name, Description, Owner, Timeline)
- [ ] No duplicate IDs
- [ ] All timeline dates are reasonable (Features: 6-9 months, Epics: ≤3 months)
- [ ] All dependencies are documented
- [ ] All [Assumption], [Open question], and [Needs validation] items are noted

---

## Export Statistics

**Summary:**
- Total Strategic Themes: [#]
- Total Features: [#]
- Total Epics: [#]
- Total User Stories: [#]
- Total Acceptance Criteria: [#]

**By Status:**
- Active: [#]
- Planned: [#]
- Not Started: [#]
- Completed: [#]

**Coverage:**
- [%] of Features have KRs
- [%] of Epics have KRs
- [%] of ACs map to Epic KRs

---

## Quick Reference: Template Dependencies

When importing, follow this order:

1. **Create Epic objects** (parent of Features)
2. **Create Feature objects** (parent of Epics in Jira)
3. **Create Epic objects** (parent of User Stories)
4. **Create User Story objects** (with Epic links)
5. **Add Acceptance Criteria** (to User Stories)
6. **Set up Sprint assignments**

---

## Related Documents

- **Requirements hierarchy:** See `03_requirement_hierarchy.md` (source of truth)
- **Jira field mapping:** See `11_templates_and_standards/jira_field_mapping.md`
- **Feature template:** See `11_templates_and_standards/feature_template.md`
- **Epic template:** See `11_templates_and_standards/epic_template.md`
- **User story template:** See `11_templates_and_standards/user_story_template.md`

---

**Generated From:** `03_requirement_hierarchy.md`

**Last Updated:** [Date]

**Last Exported To:** [Tool name and date]

**Next Export:** [Scheduled date]

**Export Owner:** [Name]

**Notes:**
- Keep `03_requirement_hierarchy.md` as the master document
- Regenerate this file when the hierarchy changes
- Use field mappings in `11_templates_and_standards/jira_field_mapping.md`
