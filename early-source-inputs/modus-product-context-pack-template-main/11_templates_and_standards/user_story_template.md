# User Story Template

Use this template for every User Story in the product roadmap. User Stories are sprint-level units of work. See `requirement_hierarchy_standard.md` for rules and validation.

---

## Story Header

**Story ID:** [Unique identifier - e.g., US-001]

**Story Title:** [Short descriptive title]

**Parent Epic:** [Epic name and ID - e.g., "E-001: Schedule Import Foundation"]

**Status:** Ready / In Progress / In Review / Done

**Assignee:** [Engineer name - leave blank if not yet assigned]

**Sprint:** [Sprint name/number - leave blank if not yet scheduled]

**Story Points:** [Estimate - leave blank if not yet estimated]

---

## User Story

**As a** [user role - who is the user?]

**I want to** [action/feature - what does the user want to do?]

**So that** [value/outcome - why do they want this?]

---

### Story Format Example

**As a** scheduling manager at a mid-size company

**I want to** upload my existing team schedule from a CSV file

**So that** I can quickly import our current schedule instead of manually re-entering everything

---

### Writing Good User Stories

**Focus on:**
- Who: Specific user role (not "the system")
- What: Action the user wants to perform
- Why: Value to the user (not technical implementation)

**Avoid:**
- "As a system, I want to..."
- Technical implementation details
- Multiple user roles in one story

---

## Story Description

**Detailed Description:**
[1-2 paragraphs explaining the story in more detail]

Example:
> The user should be able to upload a CSV file containing their current team schedule. The system should validate the CSV format, show a preview of the imported data, and allow the user to confirm or cancel the import. If there are errors in the CSV format, the system should show clear error messages pointing out what's wrong.

---

## Acceptance Criteria

**CRITICAL: Acceptance Criteria must follow Given/When/Then format and be agent-validatable.**

See `ai_readiness_gate.md` for detailed requirements. All ACs must:
- Use Given/When/Then structure
- Specify discrete, reproducible actions (not vague)
- Describe observable outcomes (UI, DOM, or API response)
- Include exact verbatim text for screen copy
- Use quantified thresholds (numbers, not descriptions)
- Include complete pre-conditions

---

### AC Template (Agent-Validatable Format)

**AC [#]:** [Brief AC title] [Maps to: E-[#].KR#]

**Given** [Complete system state before action]
- Precondition 1
- Precondition 2 (if multiple preconditions needed)

**When** [Specific, reproducible action]

**Then** [Observable outcomes]
- Outcome 1 [Include exact text if applicable]
- Outcome 2 [Include timing/threshold if applicable]

---

### AC Example (GOOD — Agent-Validatable)

**AC 1:** User can upload CSV file from computer [Maps to: E-001.KR1]

**Given** the user is viewing the Schedule Import page
AND the page has fully loaded
AND the user has a valid CSV file on their computer

**When** the user clicks the "Choose File" button
AND selects a CSV file from their file system
AND the file is less than 50 MB

**Then** the filename appears next to the button
AND a "Preview" button becomes enabled

---

**AC 2:** System validates CSV format before preview [Maps to: E-001.KR1]

**Given** a CSV file is selected
AND the file contains required columns: date, start_time, end_time, assignee

**When** the user clicks the "Preview" button

**Then** the page displays a table showing the first 5 rows of the imported data
AND each column header matches the CSV header
AND a "Confirm & Import" button appears at the bottom
AND the button is disabled until the user scrolls to the bottom

---

**AC 3:** System shows specific error message for invalid CSV [Maps to: E-001.KR1]

**Given** a CSV file is selected
AND the file is missing one or more required columns

**When** the user clicks the "Preview" button

**Then** a red error banner appears at the top of the page within 500ms
AND the banner contains the exact text "CSV is missing required columns: [list missing columns]"
AND the banner includes a close button (X)
AND the page remains on the import screen (no navigation)

---

**AC 4:** Import completes and shows success confirmation [Maps to: E-001.KR2]

**Given** the preview table is displayed
AND all data validation passed

**When** the user clicks the "Confirm & Import" button

**Then** the button becomes disabled and shows a spinner
AND the API endpoint `POST /schedules/import` is called
AND within 3 seconds, a green success banner appears at the top
AND the banner displays the exact text "Your [X] events have been imported successfully"
(where [X] is the actual count)
AND the user is redirected to the Schedule Dashboard page
AND the imported events appear in the calendar view

---

### What FAILS Agent Validation

❌ **Bad AC (vague, not testable):**
> **AC:** User can import a CSV file
> **Given** the user is on the import screen
> **When** the user uploads a CSV
> **Then** the import succeeds and a success message is shown quickly

**Problems:**
- "on the import screen" doesn't fully describe state
- "uploads a CSV" is vague (which button? file already selected?)
- "succeeds" is undefined
- "quickly" is not quantified
- "success message" doesn't specify exact text

✅ **Good AC (specific, agent-validatable):**
> See examples above

---

### AC Standards

Each acceptance criterion should be:
- **Observable:** Visible in UI, DOM, or API response
- **Testable:** Agent can verify mechanically without assumptions
- **Specific:** Trigger is discrete and reproducible
- **Quantified:** Timing, counts, sizes are numbers
- **Valuable:** Contributes to Epic KR
- **Mapped:** Links to exactly one Epic KR

---

## UX & Design Artifacts

**Required for ANY story with a visual outcome:**

### Figma Frames

- [ ] **Scoped Figma frame exists for each AC outcome** that produces a distinct visual state
  - One frame per AC outcome
  - Linked using node-level Figma URL (not the file root)
  - Example: `https://www.figma.com/file/abc123/Product?node-id=1234%3A5678`

- [ ] **All interaction states are covered:**
  - [ ] Default state (initial screen state)
  - [ ] Loading state (while data loads)
  - [ ] Error state (validation failed or API error)
  - [ ] Empty state (no data to display)
  - [ ] Success state (operation completed)

- [ ] **Copy matches ACs verbatim**
  - If AC says "Your changes have been saved", the frame shows exactly that
  - Character-for-character, including capitalization and punctuation

- [ ] **Components use design system**
  - Reference by name: "Button (Primary)", "Badge (Success)"
  - No custom-drawn equivalents
  - All variants are components, not static graphics

### Component States Matrix (For Multi-Variant Components)

If this story uses a component with multiple variants (e.g., notification banner with success/warning/error/info states):

- [ ] **Component states matrix exists in Figma**
  - Create a dedicated Figma frame showing all variants
  - Each variant is an individually linkable node
  - One node per state variant
  - Label clearly

**Example: Notification Banner States Matrix**

| State | Figma Node Link | AC Reference | Color | Icon |
|-------|---|---|---|---|
| Success | [Link] | AC 4 success outcome | Green | Checkmark |
| Warning | [Link] | AC 5 warning outcome | Yellow | Exclamation |
| Error | [Link] | AC 3 error outcome | Red | X |
| Info | [Link] | AC 7 info outcome | Blue | Info icon |

---

## Definition of Done

**Checklist - all must be true for this story to be "done":**

- [ ] Code is written according to code standards
- [ ] Code is self-reviewed for quality
- [ ] Code is peer-reviewed and approved (at least one other engineer)
- [ ] Unit tests are written and passing (target >80% code coverage)
- [ ] Integration tests are passing
- [ ] All acceptance criteria are verified as met
- [ ] QA has tested and approved the story
- [ ] Product owner has signed off
- [ ] Documentation is updated (code comments, API docs, help docs)
- [ ] No critical or high-severity bugs found
- [ ] Performance targets are met (if applicable)
- [ ] Security review completed (if applicable)
- [ ] Story can be demoed to stakeholders

---

## Dependencies & Blockers

### Story Dependencies

**This Story Requires (Upstream):**
- [Dependency 1 - e.g., "US-012: CSV parser library (Done)"]
- [Dependency 2 - e.g., "US-015: File upload API endpoint (In Progress)"]
- [Dependency 3 - e.g., "US-018: Database migration for schedule table (Not Started)"]

**Status Check:** No story can enter sprint if any upstream dependency is Not Started or Blocked

---

### External System Dependencies

**This Story Requires (External Systems) — MUST be confirmed available before sprint entry:**

- [ ] **APIs Provisioned & Available:**
  - [ ] Google Calendar API (dev/staging/prod) ✓ Status: ___
  - [ ] [Other external APIs needed] ✓ Status: ___

- [ ] **Credentials & Access:**
  - [ ] API keys configured in `.env` files ✓ Status: ___
  - [ ] Service account credentials available ✓ Status: ___
  - [ ] Test environment has necessary permissions ✓ Status: ___

- [ ] **Infrastructure & Databases:**
  - [ ] Database schema migration deployed ✓ Status: ___
  - [ ] Staging environment is available ✓ Status: ___
  - [ ] Test data seeded (if needed) ✓ Status: ___

- [ ] **Third-Party Services:**
  - [ ] [Service name] account provisioned and API working ✓ Status: ___

**Blocking Issue if ANY checkbox is unchecked:** Story cannot be picked up in sprint

---

**Blocks (Downstream):**
- [What can't start until this story is done?]
- Example: "Blocks US-020 (AI recommendations engine) and US-021 (Schedule dashboard)"

**Parallel Work:**
- [What other stories can be worked on simultaneously?]

---

## Assumptions & Unknowns

**[Assumption]** [What we're assuming about this story]

Example:
> "Users will have standard-format CSV files (date, start_time, end_time, assignee columns)"

- **If wrong:** [Impact on story]
- **How to handle:** [What we'd do if assumption is invalid]

---

**[Open Question]** [Something we don't know]

Example:
> "Should we support Excel files (.xlsx) or just CSV?"

- **Why it matters:** [Impact on story scope]
- **How we'll decide:** [Who decides, when]

---

## Technical Notes

**Implementation Approach:**
[Brief technical description of how you'll build this]

Example:
> "Use the Papa Parse library to parse CSV client-side, validate against schema, and send validated data to /api/imports endpoint. Show progress bar during import."

**Technical Decisions:**
- [Decision 1 - why we chose this approach]
- [Decision 2]

**Edge Cases to Handle:**
- [Edge case 1 - e.g., "Large files >10MB"]
- [Edge case 2 - e.g., "Special characters in names"]
- [Edge case 3 - e.g., "Duplicate entries"]

**Performance Considerations:**
- [Performance target 1 - e.g., "File upload <10 seconds for 10MB"]
- [Performance target 2]

**Security Considerations:**
- [Security 1 - e.g., "Validate file format server-side"]
- [Security 2 - e.g., "Only authenticated users can upload"]

---

## Testing Plan

**Unit Tests:**
- [Test 1 - e.g., "Test CSV parsing with valid input"]
- [Test 2 - e.g., "Test CSV parsing with invalid input"]
- [Test 3 - e.g., "Test validation of required columns"]

**Integration Tests:**
- [Test 1 - e.g., "Test end-to-end file upload and import"]
- [Test 2 - e.g., "Test database persistence of imported data"]

**Manual Testing:**
- [Test 1 - e.g., "Test with sample CSV files from real users"]
- [Test 2 - e.g., "Test error messages with various malformed CSVs"]
- [Test 3 - e.g., "Test with large files to verify performance"]

**Browser/Device Testing:**
- [Browsers: Chrome, Firefox, Safari, Edge]
- [Devices: Desktop, tablet (if applicable)]

---

## Estimate & Effort

**Story Points:** [Your estimate - if estimated]

**Time Estimate:** [Hours/days - how long you think this will take]

**Complexity:** [Simple / Medium / Complex]

**Why This Estimate:**
[Brief explanation of sizing]

Example:
> "Medium complexity - file upload is straightforward, but validation logic requires careful error handling and user messaging."

---

## Acceptance Criteria Mapping

**Verification Matrix:**

| AC | Epic KR | How We'll Verify | QA Sign-Off |
|---|---|---|---|
| AC-1 | E-001.KR1 | [How QA will verify] | [ ] |
| AC-2 | E-001.KR1 | [How QA will verify] | [ ] |
| AC-3 | E-001.KR1 | [How QA will verify] | [ ] |
| AC-4 | E-001.KR2 | [How QA will verify] | [ ] |
| AC-5 | E-001.KR1 | [How QA will verify] | [ ] |

---

## Success & Metrics

**How Will We Know This Story Succeeded?**

- [Signal 1 - e.g., "Users complete import with <5% error rate"]
- [Signal 2 - e.g., "Zero support tickets about CSV format issues"]
- [Signal 3 - e.g., "Performance benchmark met: <5 second import"]

---

## Related Stories

**Depends on:**
- [Story X - (must be done first)]

**Enabled by:**
- [Story Y - (if this story ships first, this becomes possible)]

**Related Stories:**
- [Story Z - (works on similar area but independent)]

---

## Story History

**Created:** [Date]

**Creator:** [Name]

**Last Updated:** [Date]

**Updated By:** [Name]

---

## Questions & Discussion

**Product Owner Notes:**
[Any context or notes from the PM]

**Engineering Notes:**
[Any technical notes or concerns]

**Design Notes:**
[Any design specs or mockups linked]

---

## Related Documents

- **Epic template:** See `epic_template.md`
- **Hierarchy standard:** See `requirement_hierarchy_standard.md`
- **Definition of Done:** [Link to team's Definition of Done if different]
- **Code standards:** [Link to team's code standards]
- **Design specs:** [Link to Figma or design tool if applicable]

---

**Story ID:** [US-#]

**Created:** [Date]

**Owner:** [Engineer when assigned]

**Next Step:** [To be assigned to sprint / Ready for sprint / In progress]
