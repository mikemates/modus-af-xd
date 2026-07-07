# Release Learning Map

Document what we shipped, what happened, and what we learned. This is the foundation for continue/change/stop decisions.

## Release Format

For each release, capture:
1. **What we shipped** (features and epics delivered)
2. **When it shipped** (date, sprint, quarter)
3. **What we expected** (targets and hypotheses)
4. **What actually happened** (metrics and outcomes)
5. **What we learned** (insights and signals)
6. **What we're changing** (product, strategy, or execution decisions as a result)

---

## Release 1: [Release Name/Theme]

**Release ID:** R-001

**Release Date:** [Date shipped]

**Duration:** [When we started building to when we shipped]

**Owner:** [Product Manager, Engineering Lead]

---

### What We Shipped

**Features Delivered:**
- [Feature 1] - [Brief description]
- [Feature 2] - [Brief description]

**Epics Included:**
- [Epic 1.1] - [Brief description]
- [Epic 1.2] - [Brief description]

**Key Capabilities:**
- [Capability 1]
- [Capability 2]

**Customer Impact:**
> [1-2 sentence summary of what customers can now do that they couldn't before]

---

### What We Expected

**Hypothesis:**
> "If we ship [feature], then [customer outcome], resulting in [business outcome]."

Example:
> "If we ship the scheduling dashboard, then users can find available time slots 5x faster, resulting in 30% more bookings."

**Success Criteria:**
| Metric | Target | Reason |
|--------|--------|--------|
| [Adoption metric] | [Target %] | [Why this matters] |
| [Engagement metric] | [Target value] | [Why this matters] |
| [Revenue metric] | [Target $] | [Why this matters] |

**[Assumption]** [What we were assuming about customer response]

**[Open question]** [What we expected to learn]

---

### What Actually Happened

**Shipping & Timeline:**
- **Planned launch:** [Date]
- **Actual launch:** [Date]
- **Delays:** [If any, what caused them and impact]

**Adoption Metrics:**
| Metric | Target | Actual | Status |
|--------|--------|--------|--------|
| [Metric 1] | [Target] | [Actual] | ✓ Met / ⚠ Missed / 🚀 Exceeded |
| [Metric 2] | [Target] | [Actual] | ✓ Met / ⚠ Missed / 🚀 Exceeded |

**Engagement Metrics:**
| Metric | Baseline | Current | Change |
|--------|----------|---------|--------|
| [Daily active users] | [X] | [Y] | [+Z%] |
| [Features per session] | [X] | [Y] | [+Z%] |
| [Session duration] | [X] | [Y] | [+Z%] |

**Business Metrics:**
| Metric | Baseline | Current | Impact |
|--------|----------|---------|--------|
| [Revenue] | [X] | [Y] | [+$Z] |
| [Customer retention] | [X%] | [Y%] | [+Z%] |
| [NRR] | [X%] | [Y%] | [+Z%] |

**Customer Feedback:**
- **Positive feedback:** [What users loved]
  - ["Quote from customer"]
  - ["Another quote"]
- **Negative feedback:** [What didn't work]
  - ["Issue reported"]
  - ["Another issue"]
- **Unexpected uses:** [How customers used it differently than expected]

**Critical Incidents:**
- [Issue 1] - [When, impact, resolution]
- [Issue 2] - [When, impact, resolution]

---

### What We Learned

**Key Learning 1: [Discovery about customer behavior, market, or product]**
- **What we discovered:** [The insight]
- **How we discovered it:** [Data, customer feedback, usage patterns]
- **Why it matters:** [Impact on strategy or product decisions]
- **Confidence level:** High / Medium / Low

**Key Learning 2: [Another discovery]**
[Repeat structure]

**Validated Assumptions:**
- **[Assumption from plan]** - ✓ Validated
  - Evidence: [What confirmed this]
  
**Invalidated Assumptions:**
- **[Assumption from plan]** - ✗ Disproven
  - Evidence: [What disproved this]
  - Impact: [What we need to change]

**Surprises:**
- **[Unexpected positive outcome]**
  - Why it surprised us: [What we expected vs. what happened]
  - Why it happened: [Root cause]
  - Value: [Impact on business]

- **[Unexpected negative outcome]**
  - Why it surprised us: [What we expected vs. what happened]
  - Why it happened: [Root cause]
  - Impact: [What needs to change]

---

### What We're Changing

**Continue:** [What we'll keep doing more of]
- [Decision 1] - [Why]
- [Decision 2] - [Why]

**Change:** [What we'll modify or adjust]
- [Decision 1] - [Current approach] → [New approach] - [Why]
- [Decision 2] - [Current approach] → [New approach] - [Why]

**Stop:** [What we'll stop doing]
- [Decision 1] - [Why it's no longer valuable]
- [Decision 2] - [Why it's no longer valuable]

**Product Decisions This Informs:**
- [How this learning affects the roadmap]
- [Features to prioritize/deprioritize]
- [Market assumptions to revisit]

**Strategic Implications:**
- [Does this change our business model?]
- [Does this change our target market?]
- [Does this affect competitive positioning?]

---

## Release 2: [Release Name/Theme]

[Repeat the complete release structure]

---

## Cross-Release Patterns

### Cumulative Learning

**What we've learned across all releases:**

1. **Customer behavior pattern:** [Pattern observed across multiple releases]
   - Evidence: [Examples from each release]
   - Impact: [How this affects product strategy]

2. **Market signal:** [Pattern in market response across releases]
   - Evidence: [Examples]
   - Impact: [How this affects business strategy]

3. **Technical insight:** [Pattern in how the product scales or functions]
   - Evidence: [Examples]
   - Impact: [How this affects architecture or ops]

### What Changed as a Result of Learning

| Release | Initial Hypothesis | Learning | Change Made | Impact |
|---------|---|---|---|---|
| [R-001] | [Hypothesis] | [What we learned] | [Decision] | [Outcome] |
| [R-002] | [Hypothesis] | [What we learned] | [Decision] | [Outcome] |

---

## Release Pipeline

### Upcoming Release: [Release Name]

**Planned Date:** [Date]
**Theme:** [What this release is about]
**Expected Impact:** [What we're hoping to learn or achieve]
**Key Unknowns:** [What we expect to learn]
**Related Learning from Prior Releases:** [What prior releases inform this one]

---

## Metrics Dashboard

### Overall Health

| Category | Metric | Trend | Status |
|----------|--------|-------|--------|
| **Adoption** | % of users active | 📈 | 🟢 Healthy |
| **Adoption** | New customer sign-ups | 📊 | 🟡 Watch |
| **Engagement** | Daily active users | 📉 | 🔴 Declining |
| **Retention** | Month-over-month churn | 📈 | 🟡 Slight increase |
| **Business** | ARR/Revenue | 📈 | 🟢 On track |
| **Support** | Avg resolution time | 📊 | 🟢 Stable |

---

## Related Documents

- **Business intent:** See `01_business_intent.md`
- **Value flow:** See `02_value_flow_map.md`
- **Decisions:** See `04_decision_log.md`
- **Adoption metrics:** See `07_adoption_scorecard.md`
- **Requirement hierarchy:** See `03_requirement_hierarchy.md`

---

**Last Updated:** [Date]
**Learning Captured By:** [Name]
**Next Release Date:** [Date]
