# Decision Log

Record all significant product, technical, and strategic decisions with their rationale. This becomes the institutional knowledge of why we built what we built.

## Decision Framework

When recording a decision, capture:
1. **What decision was made** (clear, specific statement)
2. **Why it was made** (the problem it solves)
3. **Who decided** (owner and stakeholders)
4. **What alternatives were considered** (what we didn't choose and why)
5. **When it was made** (date and timeline context)
6. **What it affects** (which features, requirements, teams)
7. **How we'll know if it was right** (success criteria or signals)

---

## Strategic Decisions

### Decision 1: [Business/Product Strategy Direction]

**Decision ID:** SD-001

**Decision:** [What we decided to do or not do]

**Problem Solved:** [The business question or challenge this addresses]

**Context:** [Timeline, market conditions, customer feedback, etc.]

**Owner:** [Who made the decision]

**Stakeholders:** [Who was involved in or affected by this decision]

**Alternatives Considered:**
- **Option A:** [Alternative 1] - Why we didn't choose this
- **Option B:** [Alternative 2] - Why we didn't choose this
- **Chosen:** [What we selected and why]

**Impact:**
- **Scope:** [What parts of the product/organization this affects]
- **Timeline:** [When this decision takes effect]
- **Risk:** [What could go wrong if this decision is wrong]
- **Reversibility:** [Can we undo this? How costly would that be?]

**Success Metrics:**
- [What signals this was the right decision]
- [What signals we should reconsider]

**Related Documents:**
- [References to business intent, features, etc.]

**Assumptions:**
- **[Assumption]** [What we're assuming about markets, customers, etc.]
- **[Assumption]** [Another assumption]

**Date:** [Decision made]
**Last Reviewed:** [Date]

---

### Decision 2: [Another Strategic Direction]

**Decision ID:** SD-002

[Repeat template structure]

---

## Product Decisions

### Decision: [Feature Scope or Prioritization]

**Decision ID:** PD-001

**Decision:** [What we decided about this feature/capability]

**Problem Solved:** [Why this decision was needed]

**Context:** [Customer feedback, market research, competitive pressure, etc.]

**Owner:** [PM, Product Lead]

**Alternatives Considered:**
- **Option A:** [Alternative] - Why rejected
- **Option B:** [Alternative] - Why rejected
- **Chosen:** [Selected approach and rationale]

**What This Means:**
- **In scope:** [What's included]
- **Out of scope:** [What's explicitly excluded]
- **Timing:** [When this ships]

**Feature Impact:**
- [Which feature(s) this decision affects]
- [User stories or epics that change]

**Success Metrics:**
- [How we'll know this was right]

**[Assumption]** [What we're assuming about customer adoption, willingness to pay, etc.]

**Date:** [When decided]

---

### Decision: [Another Product Direction]

**Decision ID:** PD-002

[Repeat structure]

---

## Technical Decisions

### Decision: [Architecture, Technology, or Implementation Approach]

**Decision ID:** TD-001

**Decision:** [What technical approach we chose]

**Problem Solved:** [Why this decision was needed - scalability, maintainability, performance, etc.]

**Context:** [Constraints, requirements, team expertise, timeline]

**Owner:** [Tech Lead, Engineering Manager]

**Alternatives Considered:**
- **Option A:** [Alternative 1]
  - Pros: [Benefits]
  - Cons: [Drawbacks]
- **Option B:** [Alternative 2]
  - Pros: [Benefits]
  - Cons: [Drawbacks]
- **Chosen:** [Selected approach]
  - Why: [Rationale]

**Technical Details:**
- [Architecture diagram or key components]
- [Technology choices]
- [Database schema changes]
- [Integration points]

**Trade-offs:**
- [What we gained]
- [What we sacrificed]
- [Why this trade-off is acceptable]

**Impact on Product:**
- [Which features this enables or constrains]
- [Performance characteristics]
- [Operational implications]

**Scalability/Future Implications:**
- [How this decision affects future flexibility]
- [What becomes harder/easier]
- [Technical debt, if any]

**Implementation Plan:**
- [How we'll execute this decision]
- [Rollout approach]
- [Rollback plan]

**Success Metrics:**
- [Technical metrics to validate this was right]
- [Performance targets]
- [Operational metrics]

**Date:** [When decided]

---

### Decision: [Another Technical Approach]

**Decision ID:** TD-002

[Repeat structure]

---

## Reversals & Changes

When you reverse or significantly change a prior decision, document it here with new learning.

### Changed: [Previous Decision Name]

**Original Decision ID:** [SD-001, PD-001, etc.]

**What Changed:** [What we're doing differently now]

**Why:** [What changed in the market, product, or our understanding]

**New Approach:** [The new decision and rationale]

**Impact:** [What needs to change in the product/roadmap because of this]

**Learning:** [What we learned that caused this reversal]

**Date Changed:** [When we made the change]

---

## Open Questions in Decisions

Document decisions that are still being made or where uncertainty remains:

### Pending Decision: [Topic]

**Decision Needed:** [What we need to decide]

**Why It Matters:** [Impact on the roadmap or product]

**Context:** [What we know so far]

**Options Being Considered:**
- **Option A:** [Approach and implications]
- **Option B:** [Approach and implications]
- **Option C:** [Approach and implications]

**Key Unknowns:** [What we don't know that affects this decision]

**Timeline for Decision:** [When we need to decide]

**Who Needs to Be Involved:** [Stakeholders]

**How We'll Decide:** [Decision framework or data we need]

---

### Pending Decision: [Another Topic]

[Repeat structure]

---

## Decision Impact Matrix

Quick reference to see which features/components are affected by each major decision:

| Decision | Feature 1 | Feature 2 | Feature 3 | Technical Impact |
|----------|---|---|---|---|
| [SD-001] | HIGH | MEDIUM | - | Affects architecture |
| [PD-001] | MEDIUM | - | HIGH | Minimal impact |
| [TD-001] | HIGH | HIGH | HIGH | Foundational |

---

## Related Documents

- **Business intent:** See `01_business_intent.md`
- **Value flow:** See `02_value_flow_map.md`
- **Requirements:** See `03_requirement_hierarchy.md`
- **Learning from decisions:** See `06_release_learning_map.md`

---

**Last Updated:** [Date]
**Decision Log Owner:** [Name]
**Review Cadence:** [Weekly/Bi-weekly/Monthly]
