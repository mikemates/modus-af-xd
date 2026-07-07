# AI Readiness Gate

## Overview

The **AI Readiness Gate** is a quality gate that sits between backlog refinement and sprint planning. Stories that do not pass this gate **never reach sprint planning**. This gate exists because AI agents cannot fill context gaps, infer intent from memory, or ask clarifying questions — the ticket is the agent's entire world.

**Gate Ownership:** Product Owners & Experience Designers (NOT Engineering)

**Gate Timing:** Before sprint planning

---

## Why This Gate Exists

**The Problem with Traditional Backlogs:**
- A human engineer reads a ticket, fills gaps from memory, and asks questions in Slack
- They infer intent from prior conversations and make judgment calls
- An AI agent cannot do any of this

**The Cost of Ambiguity at Scale:**
- One poorly written story = one engineer going in the wrong direction
- One poorly written story for AI agents = six agents going in six wrong directions **in parallel**
- Ambiguous acceptance criteria, missing design states, implicit business rules, and undocumented dependencies cause agents to make wrong assumptions silently, at scale, across multiple workstreams simultaneously

**Solution:** Clear, complete, agent-validatable requirements before execution begins

---

## Epic AI Readiness Criteria

An epic is **AI-ready** when a Business Analyst can derive well-formed stories from it **without asking any clarifying questions**.

### Required Epic Attributes

| # | Criteria | Owner | Validation |
|---|----------|-------|-----------|
| 1 | Problem statement is clearly articulated — what user or business pain does this solve? | PO | Story map shows the pain point |
| 2 | Success metrics are defined and measurable — how do we know the epic delivered value? | PO | KRs with targets and metrics defined |
| 3 | In-scope is explicit | PO | Clear list of capabilities included |
| 4 | Out-of-scope is equally explicit | PO | Clear list of what's deferred/excluded |
| 5 | **A walking skeleton is identifiable** — the thinnest slice that delivers real value end-to-end | PO | Can trace a user action from entry to exit |
| 6 | Dependencies on other epics are identified and sequenced | PO | Dependency map shows ordering |
| 7 | The epic can be broken into at least two independent vertical slices | PO/BA | User stories can execute in parallel |

**Most Critical:** The walking skeleton (Criterion 5). If no walking skeleton exists, stories cannot be structured as a dependency graph — everything becomes a sequential chain and parallel agent execution is impossible.

---

## Story AI Readiness Criteria

A story is **AI-ready** when an agent can implement it **from the ticket alone, without supplemental context from any person**.

### 1. Problem and Intent

**Required Format: User Story**
```
As a [SPECIFIC PERSONA],
I want to [ACTION/FEATURE],
So that [BUSINESS OUTCOME].
```

**Validation Criteria:**

- [ ] **Persona is SPECIFIC**, not generic
  - ❌ BAD: "As a user"
  - ✅ GOOD: "As a scheduling administrator managing shifts for 50+ employees"

- [ ] **"So that" is a real business outcome**, not a restatement of the feature
  - ❌ BAD: "So that I can upload a CSV file" (just repeats the feature)
  - ✅ GOOD: "So that I can get my 200-person schedule into the system in <5 minutes instead of 2 hours of manual entry"

---

### 2. Scope

**Required Sections:**

- [ ] **Single bounded outcome** — no "and also" items
  - If the story has multiple outcomes, split into separate stories
  
- [ ] **Out-of-scope is stated when ambiguity is likely**
  - Example: "We are NOT building a schedule editor in this story; users import read-only"

- [ ] **UI, API, and data layer impact is identified**
  - Example: "This adds a new endpoint `POST /schedules/import`, updates the Schedule table schema with an `imported_at` field, and adds a new React component `ScheduleImportFlow`"

---

### 3. Acceptance Criteria

**CRITICAL: Agent-Validatable Format Required**

**Every AC must follow Given/When/Then with ALL of the following:**

#### ✅ Required Elements

1. **Specific trigger** — the "When" is a discrete, reproducible action
   - ✅ GOOD: "when the user clicks the 'Upload File' button and selects a CSV file"
   - ❌ BAD: "when the user uploads a file"

2. **Observable outcome** — the "Then" describes something visible in UI, DOM, or API response
   - ✅ GOOD: "a success banner appears in the top right containing the text 'Import complete'"
   - ❌ BAD: "the import completes"

3. **Verbatim copy** — any text that appears on screen is written exactly as it should appear
   - ✅ GOOD: `Then a green banner displays with the text "Your schedule imported 247 events"`
   - ❌ BAD: "a success message is shown"

4. **Quantified thresholds** — timing, counts, and sizes are numbers, not descriptions
   - ✅ GOOD: "within 2 seconds", "500 character limit", "max 100 events per import"
   - ❌ BAD: "quickly", "large files", "reasonable timeout"

5. **Complete pre-condition** — the "Given" fully describes the system state before the action
   - ✅ GOOD: "Given the user has a valid Gmail account connected AND is viewing the Schedule Import page AND the page has fully loaded"
   - ❌ BAD: "Given the user is logged in"

---

#### ❌ What FAILS Agent Validation

```
Given the user submits the form,
When it succeeds,
Then a success message is shown quickly.
```

**Problems:**
- "submits the form" is not specific (which button? how?)
- "succeeds" is vague (what does success mean?)
- "shown quickly" is not quantified
- "success message" doesn't specify the exact text

---

#### ✅ What PASSES Agent Validation

```
Given the user has completed all required fields (Name, Email, Schedule File)
AND the user is viewing the Import Confirmation screen,
When the user clicks the "Confirm & Import" button,
Then the API returns HTTP 200
AND a green banner appears within 300ms in the top-center of the page
AND the banner contains the exact text "Your 247 events have been imported successfully"
AND the banner auto-dismisses after 5 seconds or when the user clicks the X.
```

**Why this works:**
- Specific trigger: button click identified precisely
- Specific condition: full system state described
- Observable outcomes: 4 verifiable states (HTTP response, visual appearance, timing, text, behavior)
- Quantified: 300ms, 5 seconds, exact text, exact count
- Agent can validate each part mechanically

---

#### Template: AC in Given/When/Then Format

```
**AC [#]:** [Brief description] [Maps to: E-X.KR#]

**Given** [Complete system state before action]
- Condition 1
- Condition 2
- Condition 3

**When** [Specific, reproducible action]

**Then** [Observable outcomes]
- Outcome 1 [Include exact text if applicable]
- Outcome 2 [Include timing/threshold if applicable]
- Outcome 3 [Include quantified measure]
```

---

### 4. UX and Design Artifacts

**For ANY story with a visual outcome:**

- [ ] **Scoped Figma frame exists for each AC condition** that produces a distinct visual state
  - One frame per AC outcome state
  - Linked using **node-level Figma URL** (not the file root URL)
  
- [ ] **All interaction states are covered:**
  - [ ] Default state (initial load)
  - [ ] Loading state
  - [ ] Error state
  - [ ] Empty state (no data)
  - [ ] Success state
  
- [ ] **Copy in Figma matches copy in ACs verbatim**
  - If AC says "Your changes have been saved", Figma frame shows exactly that text
  - Not "Your changes saved" or "Successfully saved"
  
- [ ] **Components reference design system by name**
  - Example: "Uses Button (Primary)" not "custom blue button"
  - No custom-drawn equivalents
  
- [ ] **Component states matrix for components with variants**
  - For example: notification banner with success/info/warning/error states
  - Create a component states matrix in Figma with individually linkable nodes
  - One node per variant state
  - Link to each state node in the story

**Example: Notification Banner Component States Matrix**

| State | Figma Link | AC Reference |
|-------|-----------|---|
| Success (green) | [Link to node] | AC 4 success outcome |
| Warning (yellow) | [Link to node] | AC 5 warning outcome |
| Error (red) | [Link to node] | AC 6 error outcome |
| Info (blue) | [Link to node] | AC 7 info outcome |

---

### 5. Dependencies

**Required Validations:**

- [ ] **Upstream stories this depends on are linked** in the ticket and their status is known
  - Story cannot start if blocking story is not done
  - List: "Blocked by US-123 (In Progress), US-124 (Done)"

- [ ] **External system dependencies are confirmed available** before the story enters the sprint
  - [ ] APIs are provisioned and responding
  - [ ] Third-party service credentials are available
  - [ ] Test environments are accessible
  - [ ] Database schemas/migrations are prepared
  - Example: "Requires Google Calendar API key (provisioned in dev/staging/prod) ✓"

---

## Role Responsibilities in the Gate

| Role | Responsibility | Timing | Gate Decision |
|------|---|---|---|
| **Product Owner** | Epic readiness: scope, walking skeleton, success metrics, dependencies | Before BA story writing | Approve epic or request changes |
| **Business Analyst** | Story decomposition, AC writing, AC validation against Given/When/Then standard | During backlog refinement | Validate AC format & completeness |
| **Experience Designer** | Scoped Figma frames, component states matrices, copy consistency | During backlog refinement | Approve visual specs or request changes |
| **QA** | Review test case strategy for each AC; confirm test cases before sprint planning | Just before sprint planning | Approve testability or request AC rewrites |
| **Engineer** | Technical planning (not backlog readiness) — reviewing story, decomposing into implementation chunks, confirming contracts between parallel workstreams | **AFTER sprint planning** | Not responsible for backlog readiness |

**Key Point:** Engineering responsibility starts AFTER sprint planning, not before. The gate is product & design responsibility.

---

## Validation Checklist: Story Is AI-Ready

Use this before marking any story ready for sprint planning:

### Problem & Intent
- [ ] Persona is SPECIFIC (not generic: "user", "admin", etc.)
- [ ] "So that" is a real business outcome, not a feature restatement
- [ ] Story is written in clear, grammatical user story format

### Scope
- [ ] Single bounded outcome (no "and also" items)
- [ ] Out-of-scope is explicitly stated when ambiguity is likely
- [ ] UI, API, and data layer impact is identified

### Acceptance Criteria
- [ ] ALL ACs follow Given/When/Then format
- [ ] ALL "Given" statements fully describe system state (not vague)
- [ ] ALL "When" statements specify exact, reproducible actions
- [ ] ALL "Then" statements are observable (visible in UI/API/DOM)
- [ ] ALL quantified values use numbers (timing: ms, counts, thresholds)
- [ ] NO vague language: "quickly", "successfully", "properly", "easily"
- [ ] Verbatim copy for any screen text matches AC exactly
- [ ] Each AC maps to exactly one Epic KR

### UX & Design
- [ ] For visual stories: Figma frames exist for every AC outcome state
- [ ] Figma frames linked using node-level URLs (not file root)
- [ ] All interaction states covered (default, loading, error, empty, success)
- [ ] Copy in Figma matches copy in ACs character-for-character
- [ ] Components reference design system (no custom workarounds)
- [ ] Component states matrices exist for multi-state components

### Dependencies
- [ ] Upstream stories are linked with their status known
- [ ] External system dependencies are confirmed available
- [ ] All APIs, credentials, and test environments are provisioned
- [ ] No unresolved external blockers

### Clarity & Completeness
- [ ] Story can be understood by someone with no prior context
- [ ] No references to Slack conversations, wiki pages, or external docs
- [ ] All assumptions are explicit (not implicit)
- [ ] All business rules are documented

---

## Gate Process Flow

```
┌─────────────────────────────┐
│  Backlog Refinement         │
│  (PO, BA, Designer, QA)     │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│  AI Readiness Gate Check    │
│  - Epic criteria ✓          │
│  - Story criteria ✓         │
│  - Design artifacts ✓       │
│  - ACs in Given/When/Then ✓ │
└──────────────┬──────────────┘
               │
      ┌────────┴────────┐
      │                 │
      ▼                 ▼
   ✓ PASS           ✗ FAIL
      │                 │
      │          (Return to refinement)
      │                 │
      ▼                 │
  Sprint Planning ◄─────┘
  (Engineering reviews
   for technical planning)
      │
      ▼
  ✓ Implementation by Agents
```

---

## FAQ

**Q: What if we don't have Figma frames?**
A: For non-visual stories (API-only, backend logic), skip the Figma requirements. For any story with a visual outcome, frames are required.

**Q: Can we have vague AC if we document it elsewhere?**
A: No. The ticket is the agent's entire world. If it's not in the ticket, it doesn't exist. Link to external docs if needed, but the ticket must be complete.

**Q: What if we're not sure about a threshold (e.g., how long should this load)?**
A: This is what refinement is for. Work with the team to define thresholds before the story reaches the gate. Use performance benchmarks, user research, or engineering estimates — but get a number.

**Q: Can one engineer review a story instead of having a gate?**
A: No. The gate is about preventing ambiguity at scale. One engineer missing something means six agents miss the same thing in parallel.

**Q: What if a story is too complex to make agent-validatable?**
A: Split it into smaller stories. If you can't write clear Given/When/Then ACs for it, it's not ready for execution.

---

## Related Documents

- **Requirement Hierarchy:** See [03_requirement_hierarchy.md](../../03_requirement_hierarchy.md)
- **Epic Template:** See [epic_template.md](epic_template.md)
- **User Story Template:** See [user_story_template.md](user_story_template.md)
- **Requirement Standards:** See [requirement_hierarchy_standard.md](requirement_hierarchy_standard.md)

---

**Last Updated:** 2026-06-24
**Version:** 1.0 (AI-Ready)
