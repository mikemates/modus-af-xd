# Jira/Linear Field Mapping

Map Product Context Pack documents to Jira and Linear fields. Use this guide when exporting from `09_backlog_export_ready.md` to your execution tool.

---

## Export Workflow

```
03_requirement_hierarchy.md (source)
        ↓
09_backlog_export_ready.md (formatted)
        ↓
Use jira_field_mapping.md (this document)
        ↓
Import to Jira / Linear
```

---

## Jira Mapping

### Project Setup

**Project Name:** [Your project name]

**Project Key:** [Your project key - e.g., "PRODUCT"]

**Issue Types We'll Use:**
- Epic (for Epics from our hierarchy)
- Feature (for Features from our hierarchy, if Jira supports)
- Story (for User Stories)
- Task (for acceptance criteria or implementation tasks)
- Bug (for issues found during development)

---

### Epic Mapping

**Jira Epic**

| Pack Component | Jira Field | Value | Format |
|---|---|---|---|
| Epic ID | Story Label | E-001 | [Epic ID] |
| Epic Name | Epic Name | [Name] | [Full epic name] |
| Parent Feature | Epic Link | F-001 | [Parent Feature ID] or parent in custom field |
| Maps to Feature KR | Description | [Epic maps to F-001.KR1] | Documented in description |
| Epic KR 1 | Custom Field: KR 1 | [KR statement] | [Full KR text] |
| Epic KR 2 | Custom Field: KR 2 | [KR statement] | [Full KR text] |
| Timeline | Sprint | [Sprint name] | [Sprint or milestone] |
| Owner | Assignee | [Engineering Lead] | [Jira user] |
| Status | Status | Active / Planned / Done | Map to your workflow |

**Jira Epic Details:**
```
Name: [Epic Name]
Key: [Will auto-generate - e.g., PRODUCT-42]
Description: 
  Epic ID: E-001
  Maps to Feature KR: F-001.KR1
  Epic KRs:
  - E-001.KR1: [KR statement]
  - E-001.KR2: [KR statement]
  
  Scope:
  - In scope: [list]
  - Out of scope: [list]
  
  Timeline: [Date] - [Date]
  Owner: [Engineering Lead]

Status: Active / Planned / Not Started
Sprint: [Sprint name or milestone]
Labels: epic, [feature-id], [theme-id]
Due Date: [Epic end date]
```

---

### Feature Mapping

**If Jira Supports "Feature" Issue Type:**

| Pack Component | Jira Field | Value |
|---|---|---|
| Feature ID | Story Label | F-001 |
| Feature Name | Feature Name | [Name] |
| Parent Theme | Epic Link | [Theme name or custom field] |
| Feature KR 1 | Custom Field: KR 1 | [KR statement] |
| Feature KR 2 | Custom Field: KR 2 | [KR statement] |
| Timeline | Sprint / Target Start | [Sprint or milestone] |
| Owner | Assignee | [PM name] |

**If Jira Doesn't Support "Feature":**
- Create a "Feature" custom issue type
- OR use Epic to represent Features (and create Epics as Stories with epic link)
- OR add features in a separate "Feature Roadmap" view

---

### User Story Mapping

**Jira Story**

| Pack Component | Jira Field | Value | Format |
|---|---|---|---|
| Story ID | Story Label | US-001 | [Story ID] |
| Story Title | Summary | [Title] | [80 char max] |
| User Story | Description | [Story format] | As a [role] I want to [action] so that [value] |
| Parent Epic | Epic Link | E-001 | [Parent Epic key] |
| AC 1 | Acceptance Criteria | [AC 1 text] | [Observable, testable description] |
| AC 2 | Acceptance Criteria | [AC 2 text] | [Observable, testable description] |
| AC 3 | Acceptance Criteria | [AC 3 text] | [Observable, testable description] |
| AC Mapping | Acceptance Criteria | [AC-1 → E-001.KR1] | Document mapping in description |
| Assignee | Assignee | [Engineer] | [Jira user or unassigned] |
| Sprint | Sprint | [Sprint name] | [Current sprint] |
| Story Points | Story Points | [#] | [Estimate: 3, 5, 8, 13, etc.] |
| Status | Status | Ready / In Progress / Done | [Your workflow] |

**Jira Story Details:**
```
Summary: [Story Title]
Key: [Will auto-generate - e.g., PRODUCT-101]

Description:
  As a [user role],
  I want to [action],
  So that [value].
  
  Acceptance Criteria:
  - [ ] AC-1: [Observable behavior] [Maps to: E-001.KR1]
  - [ ] AC-2: [Observable behavior] [Maps to: E-001.KR1]
  - [ ] AC-3: [Observable behavior] [Maps to: E-001.KR1]
  - [ ] AC-4: [Observable behavior] [Maps to: E-001.KR2]
  
  Assumptions:
  - [Assumption 1]
  - [Assumption 2]

Epic Link: [E-001]
Sprint: [Sprint name]
Assignee: [Engineer or unassigned]
Story Points: [Estimate]
Status: Ready
Labels: story, [epic-id]
```

---

### Dependencies & Linking

**Jira Linking:**

| Link Type | Usage | Example |
|---|---|---|
| "relates to" | References another story | Story A relates to Story B |
| "blocks" | Story X blocks Story Y | US-001 blocks US-002 |
| "is blocked by" | Story X is blocked by Story Y | US-002 is blocked by US-001 |
| "depends on" | Story X depends on Story Y | US-002 depends on US-001 |
| "epic-link" | Story is part of Epic | US-001 is part of E-001 |

---

### Custom Fields (Create These in Jira)

**Recommended Custom Fields:**

| Field Name | Type | Usage | Example |
|---|---|---|---|
| KR 1 | Text | Feature/Epic first KR | "Increase bookings per user from 2 to 5" |
| KR 2 | Text | Feature/Epic second KR | "Reduce data entry time to <5 min" |
| KR 3 | Text | Feature/Epic third KR | (optional) |
| Maps to KR | Text | Story or Epic maps to which Feature KR | "F-001.KR1" |
| Pack ID | Text | Store the pack ID (F-001, E-001, US-001) | "E-001" |
| Business Outcome | Text | What business outcome does this drive | "Increase revenue by 30%" |
| Epic KR 1 | Text | Epic's first KR | (for Epics) |
| Epic KR 2 | Text | Epic's second KR | (for Epics) |

---

## Linear Mapping

### Project Setup

**Project Name:** [Your project name]

**Issue Types We'll Use:**
- Issue (generic)
- Custom issue types for Epic, Feature, Story (if using Linear's custom types)

**Linear Workflow:**
```
Backlog → Todo → In Progress → In Review → Done
```

---

### Issue Mapping for Linear

**Linear Issue Structure:**

| Pack Component | Linear Field | Value |
|---|---|---|
| Epic ID | Label | epic-E-001 |
| Epic Name | Title | [Epic Name] |
| User Story | Description | [Story description and ACs] |
| Parent Epic | Relationship / Parent | [Link to parent Epic issue] |
| Acceptance Criteria | Description section | [List all ACs with mapping] |
| Assignee | Assignee | [Linear user] |
| Sprint | Cycle | [Linear cycle] |
| Story Points | Estimate | [Estimate] |
| Status | State | Backlog / Todo / In Progress / In Review / Done |

**Linear Issue Example:**
```
Title: [Story Title]
Description:
  As a [role], I want to [action], so that [value].
  
  Acceptance Criteria:
  - [ ] AC-1: [Observable behavior] (E-001.KR1)
  - [ ] AC-2: [Observable behavior] (E-001.KR1)
  - [ ] AC-3: [Observable behavior] (E-001.KR2)
  
Assignee: [Linear user]
Cycle: [Current cycle]
Estimate: [Points]
State: Backlog / Todo / In Progress / In Review / Done
Labels: [story, epic-id, theme-id]
Relationships: 
  - Parent: [E-001 Epic issue]
  - Blocks: [If applicable]
  - Depends on: [If applicable]
```

---

### Linear Labels (Create These)

**Recommended Label Structure:**
- `epic-E-001` - For all items in this epic
- `feature-F-001` - For all items in this feature
- `theme-[theme-name]` - For all items in this theme
- `kr-F-001.KR1` - Items that contribute to this KR
- `story` - All user stories
- `epic` - All epics
- `feature` - All features
- `assumption` - Contains unvalidated assumption
- `needs-validation` - Needs metric validation
- `open-question` - Contains open question

---

### Linear Relations/Dependencies

**Linear Relationship Types:**
- Parent/Child (for hierarchy)
- Blocks/Is Blocked By (for dependencies)
- Related (for loose associations)
- Duplicate (if applicable)

**Example:**
```
Story US-002 blocks Story US-003
Story US-003 relates to Story US-001
```

---

## Bulk Import Template

### For Jira

**CSV Format for Bulk Import:**

```csv
Summary,Description,Issue Type,Epic Link,Assignee,Sprint,Story Points,Labels,Status,Due Date
"[Story Title]","As a...",Story,"[E-001]","[User]","[Sprint]","[5]","epic-E-001","Ready","[Date]"
"[Epic Name]","Epic ID: E-001...",Epic,"","[User]","[Sprint]","","epic","Active","[Date]"
```

**Steps:**
1. Format export from `09_backlog_export_ready.md` as CSV
2. Import to Jira via Tools → Import issues
3. Verify all fields mapped correctly
4. Create links and custom field values post-import

---

### For Linear

**Use Linear's CSV Import:**

```csv
Title,Description,Assignee,Estimate,Labels,Cycle,State
"[Story Title]","As a...","[user@company.com]","5","epic-E-001,story","[Cycle]","Backlog"
"[Epic Name]","Epic ID: E-001...","[user@company.com]","","epic","[Cycle]","Backlog"
```

**Steps:**
1. Format export as CSV
2. Go to Project Settings → Import issues
3. Map CSV columns to Linear fields
4. Import and verify
5. Create parent/child relationships post-import

---

## Validation Checklist

Before importing to Jira/Linear:

- [ ] All Features have IDs (F-001, F-002, etc.)
- [ ] All Epics have IDs (E-001, E-002, etc.) and parent Feature
- [ ] All User Stories have IDs (US-001, US-002, etc.) and parent Epic
- [ ] All Stories have 3-5 Acceptance Criteria
- [ ] Each Epic maps to exactly one Feature KR
- [ ] Each AC maps to at least one Epic KR
- [ ] All required fields are populated
- [ ] No duplicate IDs
- [ ] Status values are valid
- [ ] Timeline is realistic
- [ ] No special characters that will break import

---

## Post-Import Steps

**After Importing to Jira/Linear:**

1. **Create parent-child relationships:**
   - Link each Story to its Epic
   - Link each Epic to its Feature
   - Link each Feature to its Theme

2. **Create KR mappings:**
   - If using custom fields, populate Feature KRs
   - If using custom fields, populate Epic KRs
   - Populate "Maps to KR" fields

3. **Create dependencies:**
   - Link dependent stories
   - Document blockers

4. **Assign to sprints:**
   - Move stories to appropriate sprints
   - Assign owners

5. **Verify:**
   - Spot-check several issues to ensure all data transferred correctly
   - Test filtering by epic, feature, KR
   - Confirm story points and estimates are visible

---

## Common Mapping Issues & Fixes

| Issue | Cause | Fix |
|-------|-------|-----|
| Stories don't link to Epics | Epic IDs don't match | Ensure Epic Link field uses correct Epic key |
| Custom fields are empty | Fields not created before import | Create custom fields first, then import |
| KR text gets truncated | Field too short | Increase custom field text length |
| Special characters break import | CSV encoding issue | Save CSV as UTF-8 |
| Dates are wrong format | Format mismatch | Use ISO format (YYYY-MM-DD) |
| Story points not imported | Points field not mapped | Check mapping includes Story Points field |

---

## Using Jira/Linear with the Pack

**Keep Jira/Linear Updated:**
- Update story status as work progresses
- Update story points after retrospectives
- Log hours/time spent (if time-tracking enabled)
- Document blockers and dependencies

**Keep the Pack Updated:**
- Update `03_requirement_hierarchy.md` with status from Jira/Linear
- Update `06_release_learning_map.md` with outcomes after release
- Update `04_decision_log.md` with technical decisions made during implementation

**Sync Process:**
- Weekly: Verify story status and progress in both systems
- After release: Capture learning and update pack
- Quarterly: Review and refresh hierarchy in pack

---

## Related Documents

- **Requirements hierarchy:** See `03_requirement_hierarchy.md`
- **Backlog export:** See `09_backlog_export_ready.md`
- **Requirement standards:** See `requirement_hierarchy_standard.md`

---

**Version:** 1.0

**Last Updated:** [Date]

**Jira Admin:** [Name]

**Linear Admin:** [Name]

**Questions?** See `10_prompt_library.md` for help with import questions
