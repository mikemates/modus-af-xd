# Feature Template

Use this template for every Feature in the product roadmap. See `requirement_hierarchy_standard.md` for rules and validation criteria.

---

## Feature Summary

**Feature ID:** [Unique identifier - e.g., F-001]

**Feature Name:** [Clear name describing customer value or outcome]

**Theme:** [Parent Strategic Theme]

**Status:** Active / Planned / Completed

**Timeline:** [Start date] - [End date] (6-9 months expected)

**Owner:** [PM name]

**Engineering Lead:** [Engineering lead name]

---

## The Value Hypothesis

### Problem We're Solving

**Customer Problem:**
> [Describe the customer's pain point in their language]

Example:
> Scheduling managers spend 20+ hours/month manually coordinating schedules across email, spreadsheets, and team chat. This creates errors, delays decisions, and frustrates the team.

**How Large Is This Problem?**
- [How many customers face this?]
- [How painful is it? (hours/week, revenue impact, user satisfaction impact)]
- [Why is this important now?]

### How We Solve It

**Our Solution:**
> [What we're building that's different]

Example:
> We're building an AI-powered scheduling assistant that learns team preferences, automatically suggests optimal schedules, and coordinates with all calendar tools in real-time.

**Why This Approach?**
- [Why this is better than alternatives]
- [What we could have done instead and why we didn't]

### Expected Outcome

**Value Hypothesis:**
> "If we [build this feature], then [customer value], which will [business outcome]."

Example:
> "If we build an AI scheduling assistant, then managers can create schedules 5x faster and with fewer errors, which will increase bookings per user by 50% and reduce scheduling-related support tickets by 40%."

---

## Feature Key Results (KRs)

### KR 1: [Business Outcome]

**KR ID:** F-[#].KR1

**KR Statement:** [Clear outcome statement]

Example:
> "Increase average bookings per user from 2 to 5 per month"

**Baseline:** [Current value - what is it today?]

**Target:** [Goal - what do we want it to be?]

**Success Metric:** [How we'll measure this]
- [Primary metric]
- [Secondary metrics to monitor]

**Owner:** [Who is accountable for this KR]

**Timeline:** [When we expect to see progress]

---

### KR 2: [Business Outcome]

**KR ID:** F-[#].KR2

[Repeat KR 1 structure]

---

### KR 3: [Business Outcome - Optional]

[Repeat KR 1 structure if you have a third KR]

---

### KR 4: [Business Outcome - Optional]

[Repeat if you have a fourth KR]

**Note:** Limit to 2-4 KRs. More dilutes focus.

---

## Feature Scope & Constraints

### In Scope (v1)

**Core Capabilities:**
- [Capability 1 - briefly describe what it does]
- [Capability 2]
- [Capability 3]

**User Workflows:**
- [Workflow 1 - e.g., "User can import existing schedule and ask AI to optimize"]
- [Workflow 2]

**Technical Scope:**
- [Integration with: e.g., "Slack, Google Calendar, Outlook"]
- [Data handling: e.g., "Process up to 1M scheduling records"]
- [Performance: e.g., "Return suggestions in <10 seconds"]

---

### Out of Scope (v2 or Later)

**Explicitly NOT in v1:**
- [Feature 1 - e.g., "Multi-location scheduling" - will be v2]
- [Feature 2 - e.g., "Mobile app" - future release]
- [Feature 3 - e.g., "Predictive analytics for future demand" - depends on data collection first]

**Why Out of Scope:**
- [Reason 1 - e.g., "Adds complexity; we want to learn with core feature first"]
- [Reason 2 - e.g., "Requires infrastructure we don't have yet"]

---

## Feature Dependencies

**Must Happen Before This Feature:**
- [Dependency 1 - e.g., "Complete data infrastructure project"]
- [Dependency 2]

**This Feature Enables (Future):**
- [What becomes possible after we ship this]
- [Future opportunities unlocked]

---

## Success Criteria & Timeline

### By Month 1-2 (Foundation Phase)
**What:** [Epic 1 ships - core capability]
**Success Signal:** [Metric target or validation milestone]

Example:
> Epic 1 ships: Users can import existing schedules
> Success: 50% of beta customers complete import in <5 minutes

### By Month 3-4 (Expansion Phase)
**What:** [Epic 2 ships - extended capability]
**Success Signal:** [Metric target]

### By Month 6-9 (Optimization Phase)
**What:** [Epic 3/4 ships - optimization and adoption]
**Success Signal:** [Metric targets from KRs]

---

## Child Epics

**Epic Mapping to Feature KRs:**

| Epic | Epic Timeline | Maps to Feature KR | Owner | Status |
|-----|---|---|---|---|
| E-[#]: [Epic Name] | [Month range] | F-[#].KR1 | [Lead] | Not Started |
| E-[#]: [Epic Name] | [Month range] | F-[#].KR2 | [Lead] | Not Started |
| E-[#]: [Epic Name] | [Month range] | F-[#].KR[#] | [Lead] | Not Started |

**Note:** Each Epic maps to exactly one Feature KR. Verify all Feature KRs have at least one Epic working toward them.

---

## Assumptions & Unknowns

### Critical Assumptions (must be true)

**[Assumption 1]:** [What we're assuming about customers/market/feasibility]

Example:
> "Managers will adopt an AI-powered solution if it reduces their scheduling time by 75%+"

- **How we'll validate:** [Test or measurement]
- **If wrong:** [Risk to the feature or roadmap]

**[Assumption 2]:** [Another critical belief]

- **How we'll validate:** [Test approach]
- **If wrong:** [Impact]

---

### Open Questions (need answers)

**[Open Question 1]:** [Something we don't know]

Example:
> "How will users handle suggestions they disagree with?"

- **Why it matters:** [Impact on UX and adoption]
- **How we'll answer:** [Research approach - user testing, analytics, etc.]

**[Open Question 2]:** [Another unknown]

- **Why it matters:** [Impact]
- **How we'll answer:** [Research approach]

---

### Items to Validate

**[Needs Validation 1]:** [Something we decided but should confirm works]

Example:
> "Target adoption rate of 60% by month 3"

- **What would validate it:** [Data or milestone]
- **Timeline:** [When we'll know]

---

## Market & Customer Context

**Target Customer Segment:**
[Description - company size, industry, role]

**Problem Frequency:** [How often do they face this problem?]

**Willingness to Pay:** [How much would they pay? What's the business case for them?]

**Competitive Landscape:** 
- [Who else solves this?]
- [How are we different?]

**Market Timing:** [Why is now the right time for this feature?]

---

## Success Definition

### We'll Know We're Winning If:

1. **KR 1 Progress:** [Metric reaches X% of target by month 3]
2. **KR 2 Progress:** [Metric reaches X% of target by month 3]
3. **Customer Feedback:** [Specific positive feedback we expect to hear]
4. **Usage Pattern:** [How users should be adopting this feature]
5. **Support Signal:** [Support tickets should be about [specific topics], not [problems].]

### We'll Know We Should Pivot If:

1. **KR 1 Lagging:** [If metric doesn't reach X% by month 3]
2. **Customer Feedback:** [If we hear [specific negative feedback]]
3. **Usage Gap:** [If adoption is <X% by month 4]
4. **Technical Blocker:** [If [technical issue] can't be resolved]

---

## Metrics & Tracking

### Leading Indicators (Usage, Engagement)

| Metric | Target | Baseline | Timeline |
|--------|--------|----------|----------|
| [Activation rate] | [X%] | [Current %] | [By month 2] |
| [Daily active users] | [#] | [Current #] | [By month 3] |
| [Workflows completed] | [# per user per week] | [Current] | [By month 3] |

### Lagging Indicators (Business Outcomes)

| Metric | Target | Timeline |
|--------|--------|----------|
| [KR 1 metric] | [Target] | [By month 6] |
| [KR 2 metric] | [Target] | [By month 6] |

---

## Risks & Mitigation

| Risk | Likelihood | Impact | Mitigation |
|------|---|---|---|
| [Risk 1] | High/Med/Low | High/Med/Low | [How we'll mitigate] |
| [Risk 2] | [Likelihood] | [Impact] | [Mitigation] |

**Example:**
| Risk | Likelihood | Impact | Mitigation |
|------|---|---|---|
| Customers reject AI suggestions | Medium | High - feature won't drive usage | User testing with real managers early; iterate on UX |
| Integration with Slack breaks | Low | Medium - reduces accessibility | Early integration testing; fallback to email |

---

## Roadmap Context

### Strategic Importance

**Why We're Building This Now:**
[Context - customer feedback, competitive pressure, market opportunity, etc.]

**How This Advances Our Strategy:**
[How this feature supports the broader theme/business strategy]

**Sequencing:**
[Does this need to ship before/after other features?]

---

### Related Features & Products

**Features This Builds On:**
[What existing features/capabilities does this leverage?]

**Features That Build On This:**
[What future features will be enabled by this?]

---

## Success Review

### Month 1-2 Review
**Questions to Answer:**
- Are we on track for core Epic 1 timeline?
- Is customer feedback positive?
- Are assumptions holding up?

**Go/No-Go Decision:**
- Proceed / Proceed with modifications / Pivot

### Month 3-4 Review
**Questions to Answer:**
- Are KR 1 and KR 2 tracking toward targets?
- Are leading indicators healthy?
- Are we hitting adoption targets?

### Month 6 Review
**Questions to Answer:**
- Have we achieved the value hypothesis?
- What did we learn?
- Do we continue, modify, or sunset this feature?

---

## Related Documents

- **Requirement hierarchy:** See `03_requirement_hierarchy.md`
- **Hierarchy standard:** See `requirement_hierarchy_standard.md`
- **Epic template:** See `epic_template.md`
- **Business intent:** See `01_business_intent.md` (context)
- **Value flow:** See `02_value_flow_map.md` (connects to outcomes)

---

**Feature ID:** [F-#]

**Created:** [Date]

**Owner:** [PM name]

**Last Updated:** [Date]

**Next Review:** [Date]
