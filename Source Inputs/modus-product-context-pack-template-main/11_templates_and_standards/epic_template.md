# Epic Template

Use this template for every Epic in the roadmap. Epics are ≤3 month execution units that map to Feature KRs. See `requirement_hierarchy_standard.md` for rules.

---

## Epic Summary

**Epic ID:** [Unique identifier - e.g., E-001]

**Epic Name:** [Clear name describing the epic's scope]

**Parent Feature:** [Feature name and ID - e.g., "Feature F-001: AI Scheduling Assistant"]

**Maps to Feature KR:** [Which Feature KR does this Epic drive? - e.g., "F-001.KR1"]

**Status:** Not Started / In Progress / Completed

**Timeline:** [Start date] - [End date] (target: ≤3 months, typically 6-8 weeks)

**Owner:** [Engineering Lead name]

---

## Epic Scope & Value

### What This Epic Delivers

**Epic Objective:**
> [1-2 sentences describing what this epic delivers and why it matters]

Example:
> "Build the core scheduling input flow that lets managers import existing schedules from Google Calendar, Outlook, and CSV files. This is the foundation for all AI recommendations."

**Why This Epic First?**
- [Why this epic is prioritized in the feature]
- [What this unblocks for other epics]
- [How this validates core assumptions]

---

### Walking Skeleton

**What is a Walking Skeleton?**
The thinnest end-to-end slice that delivers real value. If users can complete one journey from entry point to value realization, you have a walking skeleton.

**This Epic's Walking Skeleton:**
[Describe the user's end-to-end path from starting the feature to achieving the outcome. This is NOT the entire feature — it's the minimal viable path.]

Example:
> "A manager logs in → selects 'Import Schedule' → uploads a CSV file → sees a preview of 5 events → clicks 'Confirm' → sees success message. The schedule is now in the system and ready for AI analysis."

**Why This Walking Skeleton First?**
[Explain why starting with this path unblocks other epics or validates critical assumptions]

Example:
> "This validates that our CSV import works end-to-end before we build the AI recommendations engine. If we can't get schedules into the system, recommendations don't matter."

---

### Connection to Feature KR

**Parent Feature KR:** [Feature KR statement - e.g., "Increase bookings per user from 2 to 5"]

**How This Epic Drives the KR:**
[Explain the theory of change - how does completing this epic move the needle on the Feature KR?]

Example:
> "By making it easy to import existing schedules, managers can see the AI suggestions immediately. This speeds up the workflow, which leads to more frequent scheduling (higher bookings per user)."

---

## Epic Key Results (KRs)

### Epic KR 1: [Outcome This Epic Optimizes For]

**KR ID:** E-[#].KR1

**KR Statement:** [Clear outcome describing progress toward Feature KR]

Example:
> "Achieve 50% activation rate (% of beta customers who complete an import) within 8 weeks"

**Baseline:** [Current value]

**Target:** [Goal]

**Success Metric:** [How we'll measure]
- [Primary metric]
- [Secondary metrics]

**Owner:** [Who is accountable]

---

### Epic KR 2: [Another Outcome]

**KR ID:** E-[#].KR2

[Repeat KR 1 structure]

Example:
> "Complete import workflow in <5 minutes for 95% of users (measured in beta)"

---

### Epic KR 3: [Optional]

[Repeat if you have a third KR]

**Note:** Limit to 2-4 KRs per Epic.

---

## In-Scope & Out-of-Scope

### In Scope (This Epic)

**Core Capabilities:**
- [Capability 1 - e.g., "Users can upload CSV schedule file"]
- [Capability 2 - e.g., "System can parse Google Calendar ICS export"]
- [Capability 3 - e.g., "System validates schedule data and shows error messages"]

**User Workflows:**
- [Workflow 1 - e.g., "User connects their Google Calendar account via OAuth"]
- [Workflow 2 - e.g., "User uploads CSV file and system maps columns"]
- [Workflow 3 - e.g., "User reviews imported schedule before confirming"]

**Technical Scope:**
- [Integration with: Google Calendar API, Outlook API, file upload]
- [Data validation and transformation rules]
- [Error handling and user messaging]

---

### Out of Scope (Later Epic or Future)

**Explicitly NOT in This Epic:**
- [Feature 1 - e.g., "AI suggestions" - that's Epic 2]
- [Feature 2 - e.g., "Manual schedule editor" - deferred to Epic 3]
- [Feature 3 - e.g., "Integration with ADP payroll" - future]

**Why Deferred:**
- [Reason 1 - e.g., "Want to validate import flow works first"]
- [Reason 2 - e.g., "Requires additional infrastructure not ready yet"]

---

## User Stories

**Epic Contains:**

| Story ID | Title | Owner | Timeline | Status |
|----------|-------|-------|----------|--------|
| US-[#] | [Story title] | [Engineer] | [Sprint #] | Not Started |
| US-[#] | [Story title] | [Engineer] | [Sprint #] | Not Started |
| US-[#] | [Story title] | [Engineer] | [Sprint #] | Not Started |

**Total: [#] User Stories**

[See epic_detailed_user_stories section below for full user story details]

---

## Epic Dependencies

**This Epic Requires:**
- [Dependency 1 - e.g., "Development account with Google/Microsoft"]
- [Dependency 2 - e.g., "API keys and credentials"]
- [Dependency 3 - e.g., "Staging environment for testing integrations"]

**Blocks (What Waits for This):**
- [Waiting Epic 1 - e.g., "Epic E-002: AI Recommendation Engine" - can't start until import works]
- [Waiting Epic 2]

**Timeline Considerations:**
- [Critical path items that affect delivery]
- [Parallel work that can happen simultaneously]

---

## Success Criteria & Milestones

### Week 1-2 (Discovery & Design)
**What:** [User research, technical design, architecture]
**Completion Signal:** [Design approval, dependencies identified]

### Week 3-4 (Core Implementation)
**What:** [Build core import flows]
**Completion Signal:** [MVP working end-to-end in dev environment]

### Week 5-6 (Integration & Polish)
**What:** [Google/Outlook integration, error handling, UX polish]
**Completion Signal:** [All integrations working, error messages clear]

### Week 7-8 (Testing & Hardening)
**What:** [QA testing, performance optimization, bug fixes]
**Completion Signal:** [Ready for beta launch]

**Final Epic KRs Met:**
- [ ] Epic KR 1: [Metric achieved]
- [ ] Epic KR 2: [Metric achieved]

---

## Assumptions & Unknowns

### Key Assumptions

**[Assumption 1]:** [What we're assuming about feasibility or customer behavior]

Example:
> "CSV uploads will represent 50% of imports; Google Calendar will be 40%; Outlook 10%"

- **How we'll validate:** [How we'll test]
- **If wrong:** [Risk to timeline/KRs]

**[Assumption 2]:** [Another assumption]

- **How we'll validate:** [Test approach]
- **If wrong:** [Impact]

---

### Open Questions

**[Open Question 1]:** [Something we don't know]

Example:
> "How should we handle scheduling conflicts in the imported data?"

- **Why it matters:** [Impact on UX and data quality]
- **How we'll answer:** [Design decision, user feedback, etc.]

---

### To Validate

**[Needs Validation 1]:** [Something we decided but should confirm]

Example:
> "Target of <5 minute import time needs to be validated with real CSV files"

- **What would validate:** [Data or milestone]
- **When:** [Timeline]

---

## Technical Approach

### Architecture & Design

**Technical Decision:**
[Brief summary of technical approach - what we're building and how]

Example:
> "We'll use the Google Calendar API for OAuth, parse CSV with Papa Parse library, and validate against scheduling rules we define. All import logic runs server-side."

**Why This Approach:**
[Justification - security, performance, maintainability, etc.]

**Risks & Mitigations:**
- [Risk 1 - e.g., "Rate limits on Google API"] - [Mitigation: Cache, queuing]
- [Risk 2 - e.g., "Large file uploads"] - [Mitigation: Chunking, progress feedback]

**Testing Strategy:**
- [Unit tests: e.g., "CSV parsing logic"]
- [Integration tests: e.g., "Google API integration"]
- [Manual testing: e.g., "End-to-end user flows"]

---

### Implementation Notes

**Data Model:**
[Describe how import data is structured in the system]

**API Integrations:**
- [Integration 1: Google Calendar API - OAuth, read access]
- [Integration 2: Outlook API - OAuth, read access]
- [File handling: CSV validation and parsing]

**Performance Targets:**
- [File upload: <10 seconds for 10MB file]
- [CSV parsing: <5 seconds for 1000 events]
- [Import flow: <30 seconds end-to-end]

---

## Definition of Done

Epic is done when:
- [ ] All User Stories are complete (passed Definition of Done)
- [ ] All Epic KRs are met
- [ ] All acceptance criteria pass
- [ ] QA has tested and approved
- [ ] Product owner has signed off
- [ ] Security review completed (if needed)
- [ ] Performance benchmarks met
- [ ] Documentation is updated
- [ ] No critical or high bugs outstanding

---

## Metrics & Tracking

### Leading Indicators (Usage)

| Metric | Target | Owner |
|--------|--------|-------|
| [Import activation] | [X%] | [Owner] |
| [Avg import time] | [<X seconds] | [Owner] |
| [Successful imports] | [X%] | [Owner] |

### Lagging Indicators (Outcome)

| Metric | Target | Timeline |
|--------|--------|----------|
| [Epic KR 1 metric] | [Target] | [By end of epic] |
| [Epic KR 2 metric] | [Target] | [By end of epic] |

---

## Risk Register

| Risk | Likelihood | Impact | Mitigation |
|------|---|---|---|
| [Risk 1] | High/Med/Low | High/Med/Low | [How we'll mitigate] |
| [Risk 2] | [L] | [I] | [Mitigation] |

**Example:**
| Risk | Likelihood | Impact | Mitigation |
|------|---|---|---|
| Google API rate limits | Medium | High - blocks users | Implement request batching and queuing |
| Large schedule uploads fail | Low | Medium - poor UX | Add file size warnings, chunked upload |
| Users don't understand CSV format | Medium | High - low adoption | Provide CSV template, clear error messages |

---

## Epic Review & Learning

### At 2 Weeks
**Questions:**
- Are we on track with design and discovery?
- Any technical blockers emerging?
- Do we need to adjust scope?

### At 4 Weeks
**Questions:**
- Is core implementation on track?
- Are integrations working?
- Are epic KRs likely to be achieved?

### At Epic Completion
**Questions:**
- Did we achieve the Epic KRs?
- What did we learn about customers and product?
- Are assumptions validated?
- What should we do differently on the next epic?

---

## Related Documents

- **Requirement hierarchy:** See `03_requirement_hierarchy.md`
- **Hierarchy standard:** See `requirement_hierarchy_standard.md`
- **Feature template:** See `feature_template.md`
- **User story template:** See `user_story_template.md`
- **Decision log:** See `04_decision_log.md` (for technical decisions in this epic)

---

**Epic ID:** [E-#]

**Created:** [Date]

**Owner:** [Engineering Lead]

**Last Updated:** [Date]

**Next Review:** [Date]
