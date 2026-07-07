# Requirement Hierarchy

Strategic Themes → Features → Epics → User Stories

This is the executable roadmap. Use this document to plan what we're building and when. See `11_templates_and_standards/requirement_hierarchy_standard.md` for rules and validation.

---

## 🚪 AI Readiness Gate

**Before ANY story reaches sprint planning, it must pass the AI Readiness Gate.**

Stories that do not pass this gate **never reach sprint planning**. This gate exists because AI agents cannot fill context gaps, infer intent from memory, or ask clarifying questions — the ticket is the agent's entire world.

**Gate Owned By:** Product Owners & Experience Designers (NOT Engineering)

**Gate Timing:** Between backlog refinement and sprint planning

**See:** `11_templates_and_standards/ai_readiness_gate.md` for detailed criteria, validation checklists, and role responsibilities

### Quick Gate Checklist

**Epic Must Pass:**
- [ ] Problem statement clearly articulated
- [ ] Success metrics defined and measurable (via KRs)
- [ ] In-scope is explicit
- [ ] Out-of-scope is explicit
- [ ] **Walking skeleton identified** (thinnest end-to-end slice)
- [ ] Dependencies identified and sequenced
- [ ] Can be broken into ≥2 independent vertical slices

**Story Must Pass:**
- [ ] Persona is SPECIFIC (not generic)
- [ ] "So that" is a real business outcome (not feature restatement)
- [ ] Single bounded outcome (no "and also")
- [ ] All ACs in Given/When/Then format with specific triggers, observable outcomes, quantified thresholds
- [ ] No vague language ("quickly", "properly", "easily")
- [ ] UI/API/data layer impact identified
- [ ] For visual stories: Figma frames linked with all interaction states
- [ ] External system dependencies confirmed available

---

## Role Responsibilities

| Role | Responsibility | When | Success Criteria |
|------|---|---|---|
| **Product Owner** | Epic readiness: problem statement, scope, walking skeleton, success metrics, dependencies | Before BA writes stories | Epic passes gate criteria |
| **Business Analyst** | Story decomposition, AC writing in Given/When/Then, AC validation | During backlog refinement | All ACs agent-validatable; no gaps |
| **Experience Designer** | Figma frames, component states matrices, copy consistency | During backlog refinement | All visual specs linked; copy matches verbatim |
| **QA** | Test case review strategy; confirm test cases before sprint | Just before sprint planning | Each AC has corresponding test case |
| **Engineer** | Technical planning (NOT backlog readiness) — reviewing story, decomposing into impl chunks | **AFTER sprint planning** | Not responsible for backlog quality |

**Key Point:** Engineering responsibility starts AFTER sprint planning, not before. The gate is Product & Design responsibility.

---

## Hierarchy Overview

```
Strategic Theme (business investment area, ~12 months)
├─ Feature 1 (6-9 month deliverable, tied to business outcomes)
│  ├─ Feature KR 1 (Key Result for this feature)
│  ├─ Epic 1.1 (≤3 months, maps to Feature KR 1)
│  │  ├─ Epic KR 1.1.a
│  │  ├─ Epic KR 1.1.b
│  │  └─ User Story 1.1.1
│  │     └─ AC 1 [maps to Epic KR 1.1.a]
│  │
│  └─ Epic 1.2 (≤3 months, maps to Feature KR 2)
│     ├─ Epic KR 1.2.a
│     └─ User Story 1.2.1
│        └─ AC 1 [maps to Epic KR 1.2.a]
│
└─ Feature 2 (6-9 month deliverable, tied to business outcomes)
   └─ [Similar structure]
```

## Strategic Theme 1: [Business Investment Area]

**Theme Duration:** [Total timeline for this theme]
**Expected Impact:** [Business outcomes from this theme]
**Owner:** [Who is responsible for delivery]

### Theme Assumptions
- **[Assumption]** [What we're assuming about market/customer/technical feasibility]
- **[Assumption]** [Another critical assumption]

---

## Strategic Theme 1: Feature 1

### Feature Summary

**Feature Name:** [Clear, outcome-oriented name]

**Feature Duration:** 6-9 months

**Feature Owner:** [PM/Engineering lead]

**Business Objective:** [What business outcome does this feature drive? Connect to 01_business_intent.md and 02_value_flow_map.md]

**Value Hypothesis:** 
> "If we [build this feature], then [customer outcome], which will lead to [business outcome]."

Example:
> "If we build automated scheduling that reduces booking time from 15 minutes to 30 seconds, then customers will schedule more frequently (+50% bookings), which will increase monthly recurring revenue by $X."

### Feature Key Results (KRs)

Every Feature must have measurable KRs tied to business outcomes. Each Epic should map to exactly one Feature KR.

| KR ID | KR Statement | Target | Success Metric | Owner |
|-------|----|----|--|--|
| F1.KR1 | [Business outcome we're optimizing for] | [Target value] | [How we measure] | [Owner] |
| F1.KR2 | [Another outcome] | [Target value] | [How we measure] | [Owner] |
| F1.KR3 | [Another outcome] | [Target value] | [How we measure] | [Owner] |

**Example:**
| KR ID | KR Statement | Target | Success Metric | 
|-------|----|----|--|
| F1.KR1 | Increase booking frequency for power users | +50% bookings | Weekly bookings per user, cohort analysis |
| F1.KR2 | Achieve 40% adoption within target segment | 40% | % of eligible users activating feature |

### Feature Scope & Constraints

**In scope:**
- [What we're building]
- [What's included]

**Out of scope:**
- [What we're explicitly not building in v1]
- [What's deferred to later]

**Assumptions & Unknowns:**
- **[Assumption]** [What we're assuming about feasibility, market response, etc.]
- **[Open question]** [What we need to answer before starting]
- **[Needs validation]** [What we'll need to confirm works in practice]

---

## Strategic Theme 1: Feature 1: Epic 1.1

### Epic Summary

**Epic Name:** [Sprint-ready breakdown of the feature]

**Epic Duration:** ≤3 months (target: 1-2 quarters)

**Maps to Feature KR:** F1.KR1

**Epic Owner:** [Engineering lead]

**Epic Scope:**
[1-2 paragraph description of what this epic delivers. This should be a meaningful, shippable slice of the feature that directly supports one Feature KR.]

### Epic Key Results

Each Epic must have measurable KRs. Each User Story acceptance criterion must map to at least one Epic KR.

| KR ID | KR Statement | Target | Success Metric |
|-------|----|----|--|
| E1.1.KR1 | [Outcome we're optimizing for] | [Target] | [Metric] |
| E1.1.KR2 | [Another outcome] | [Target] | [Metric] |

**Example for scheduling epic:**
| KR ID | KR Statement | Target | Success Metric |
|-------|----|----|--|
| E1.1.KR1 | Reduce scheduling time from 15 min to <1 min | 95th percentile: <60s | Timing data in analytics |
| E1.1.KR2 | Achieve 35% adoption of auto-scheduling | 35% | Feature activation rate |

### Implementation Plan

| User Story | Sprint | Owner | Status |
|----|----|--|--|
| [US-1: See below] | Q1-Sprint1 | [Engineer] | Not Started |
| [US-2: See below] | Q1-Sprint2 | [Engineer] | Not Started |

---

### User Story 1.1.1

**User Story ID:** F1.E1.1-US1

**Epic:** Feature 1, Epic 1.1

**User Story:**
```
As a [specific persona],
I want to [action/feature],
So that [business value/outcome].
```

**Example:**
```
As a scheduling administrator managing shifts for 50+ employees,
I want to import my existing Google Calendar schedule,
So that I can get my 200+ existing events into the system in <5 minutes instead of 2 hours of manual entry.
```

**Acceptance Criteria (Given/When/Then Format — Agent-Validatable):**

Each AC must follow this format and be specific, observable, and quantified:

**AC 1:** [Brief description] [Maps to Epic KR E1.1.KR1]

Given [Complete system state]
- Condition 1
- Condition 2

When [Specific, reproducible action]

Then [Observable outcomes]
- Outcome 1 [include exact text if applicable]
- Outcome 2 [include timing if applicable]

**Example:**

**AC 1:** User can select CSV file from computer [Maps to E1.1.KR1]

Given the user is viewing the Schedule Import page
AND the page has fully loaded
AND the user has a valid CSV file on their computer

When the user clicks the "Choose File" button
AND selects a CSV file from their file system

Then the filename appears next to the button in gray text
AND a "Preview" button becomes enabled

---

**AC 2:** System validates CSV format before preview [Maps to E1.1.KR1]

Given a CSV file is selected
AND the file contains required columns: date, start_time, end_time, assignee

When the user clicks the "Preview" button

Then the page displays a table showing the first 5 rows
AND each column header matches the CSV header
AND a "Confirm & Import" button appears at the bottom

---

**AC 3:** System shows error for invalid CSV [Maps to E1.1.KR1]

Given a CSV file is selected
AND the file is missing one or more required columns

When the user clicks the "Preview" button

Then a red error banner appears within 500ms
AND the banner contains the exact text "CSV is missing required columns: [list names]"
AND the page remains on the import screen

---

**AC 4:** Import completes successfully [Maps to E1.1.KR2]

Given the preview table is displayed
AND all data validation passed

When the user clicks "Confirm & Import"

Then the button shows a spinner
AND the API endpoint POST /schedules/import is called
AND within 3 seconds, a green banner appears
AND the banner displays "Your [X] events have been imported successfully" (where [X] is the count)
AND the user is redirected to the Schedule Dashboard

**Definition of Done:**
- [ ] Code reviewed and merged
- [ ] Unit tests pass (target >80% coverage)
- [ ] Integration tests pass
- [ ] All acceptance criteria verified as met
- [ ] QA has tested and approved
- [ ] Product owner has signed off
- [ ] Documentation updated
- [ ] No critical bugs reported
- [ ] Figma frames match implementation (if visual story)
- [ ] External dependencies confirmed working in sprint environment

---

### User Story 1.1.2

[Repeat structure for each user story in the epic]

---

## Strategic Theme 1: Feature 1: Epic 1.2

[Repeat epic structure for each epic in the feature]

---

## Strategic Theme 1: Feature 2

[Repeat feature structure for each feature in the theme]

---

## Roadmap Timeline

### Q[N] - [Quarter]

**Theme:** [Theme name]
**Features planned:** [Feature list]
**Epics targeted:** [Epic list]
**Expected outcomes:** [What we expect to learn/achieve]

**[Assumption]** [Assumptions about delivery timeline or market impact]

---

### Q[N+1] - [Quarter]

[Repeat for next quarter]

---

## Dependency Map

```
[Visualize dependencies between epics]

Theme 1
├─ Feature 1
│  ├─ Epic 1.1 (can start immediately)
│  ├─ Epic 1.2 (depends on Epic 1.1 completion)
│  └─ Epic 1.3 (depends on Epic 1.2)
│
└─ Feature 2
   ├─ Epic 2.1 (can start immediately)
   └─ Epic 2.2 (parallel with Epic 1.2)
```

## Validation Checklist

**Use this to ensure the hierarchy meets AI Readiness standards before execution:**

### Epic AI Readiness Validation

- [ ] **Problem Statement** — Clearly articulates what user or business pain this epic solves
- [ ] **Success Metrics** — Defined and measurable via Key Results (KRs)
- [ ] **In-Scope** — Explicit list of what's included
- [ ] **Out-of-Scope** — Explicit list of what's deferred
- [ ] **Walking Skeleton** — Identified (the thinnest end-to-end slice delivering real value)
- [ ] **Dependencies** — Other epics identified and sequenced
- [ ] **Vertical Slices** — Can be broken into ≥2 independent slices (enables parallel execution)

### Feature-Level Validation

- [ ] Each Feature has a clear, outcome-driven value hypothesis
- [ ] Each Feature has 2-4 measurable KRs tied to business outcomes
- [ ] Each Epic maps to exactly one Feature KR
- [ ] Timeline is realistic (Features: 6-9 months, Epics: ≤3 months)

### Story-Level Validation

**Problem & Intent:**
- [ ] Persona is SPECIFIC, not generic ("admin managing shifts" not "user")
- [ ] "So that" is a real business outcome, NOT a restatement of the feature
- [ ] Story follows user story format: As a [persona], I want [action], So that [outcome]

**Scope:**
- [ ] Single bounded outcome (no "and also" items)
- [ ] Out-of-scope is explicitly stated when ambiguity is likely
- [ ] UI, API, and data layer impact is identified

**Acceptance Criteria — CRITICAL for AI Readiness:**
- [ ] ALL ACs follow Given/When/Then format
- [ ] ALL "Given" statements fully describe system state (not vague)
- [ ] ALL "When" statements specify exact, reproducible actions
- [ ] ALL "Then" statements describe observable outcomes (UI, DOM, or API)
- [ ] ALL quantified values use numbers (timing, counts, sizes — NOT descriptions)
- [ ] NO vague language: "quickly", "successfully", "properly", "easily", "reasonable"
- [ ] Verbatim copy for any screen text matches ACs exactly
- [ ] Each AC maps to exactly one Epic KR

**UX & Design (For Visual Stories):**
- [ ] Figma frame exists for each AC outcome state that produces a distinct visual
- [ ] Figma frames linked using node-level URLs (not file root)
- [ ] All interaction states covered: default, loading, error, empty, success
- [ ] Copy in Figma matches copy in ACs character-for-character
- [ ] Components reference design system by name (no custom workarounds)
- [ ] Component states matrices exist for multi-variant components

**Dependencies:**
- [ ] Upstream stories linked with their current status known
- [ ] External system dependencies confirmed available (APIs, credentials, environments)
- [ ] All APIs provisioned and responding
- [ ] Test environments accessible
- [ ] Database schemas/migrations prepared
- [ ] No unresolved external blockers

**Completeness:**
- [ ] Story can be understood by someone with no prior context
- [ ] No references to Slack conversations, wiki pages, or external docs
- [ ] All assumptions are explicit (not implicit)
- [ ] All business rules are documented
- [ ] Story is not dependent on undocumented tribal knowledge

### Dependency & Sequencing Validation

- [ ] No circular dependencies between epics
- [ ] All stories have known upstream/downstream relationships
- [ ] Walking skeleton stories can start immediately
- [ ] Dependent stories blocked until prerequisites are done
- [ ] Timeline respects dependency sequencing

---

## Backlog

### Planned but Unscheduled

[Features/Epics planned for future quarters but not yet scheduled]

### Ideas & Concepts

[Long-term themes or features being considered but not yet committed]

### Deferred

[Features we decided not to build and why]

---

## Related Documents

- **AI Readiness Gate:** See `11_templates_and_standards/ai_readiness_gate.md` — Detailed gate criteria, validation checklists, and role responsibilities
- **Business intent:** See `01_business_intent.md`
- **Value flow:** See `02_value_flow_map.md`
- **Decision log:** See `04_decision_log.md`
- **Export ready:** See `09_backlog_export_ready.md`
- **Templates:** See `11_templates_and_standards/`
  - `epic_template.md` — For writing epics
  - `user_story_template.md` — For writing user stories
  - `requirement_hierarchy_standard.md` — Detailed standards and rules

---

**Last Updated:** [Date]
**Reviewed by:** [Name]
**Next Review:** [Date]
