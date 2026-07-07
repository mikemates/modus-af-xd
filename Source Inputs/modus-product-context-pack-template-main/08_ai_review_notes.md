# AI Review Notes

Summary of Claude/AI analysis, feedback, and recommendations for the Product Context Pack. Use this to track validation, identify gaps, and document improvement areas.

## Most Recent Review

**Review Date:** [Date]

**Reviewer:** Claude Haiku (via GitHub Copilot)

**Review Scope:** [What was reviewed: full pack, specific documents, requirements hierarchy, etc.]

---

### ✓ Strengths

*Areas where the pack is well-executed:*

- **[Strength 1]** - [Why this is strong]
- **[Strength 2]** - [Why this is strong]
- **[Strength 3]** - [Why this is strong]

---

### ⚠️ Gaps & Unknowns

*Explicit gaps that need resolution before execution:*

| Gap | Location | Impact | Priority | Action |
|-----|----------|--------|----------|--------|
| [Gap 1: Missing info about...] | [File/Section] | [How it affects roadmap] | HIGH / MED / LOW | [What to do] |
| [Gap 2] | [File/Section] | [Impact] | [Priority] | [Action] |

**[Assumption] Items to Validate:**
- [Assumption from pack] - [Why it needs validation]
- [Another assumption] - [Why it needs validation]

**[Open Question] Items to Answer:**
- [Question from pack] - [Why it's important]
- [Another question] - [Why it's important]

**[Needs Validation] Items:**
- [Item from pack] - [What needs to be confirmed]
- [Another item] - [What needs to be confirmed]

---

### 🔄 Alignment Issues

*Inconsistencies or disconnects between documents:*

| Issue | Documents | Current State | Recommended Fix |
|-------|-----------|---|---|
| [Misalignment 1] | [Doc A] vs [Doc B] | [Current state] | [Recommended fix] |
| [Misalignment 2] | [Doc A] vs [Doc B] | [Current state] | [Recommended fix] |

---

### 🎯 Hierarchy Validation

**Parent-Child Relationships:**
- [✓ / ⚠️ / ✗] Strategic Themes properly map to Features
- [✓ / ⚠️ / ✗] Features have clear value hypotheses
- [✓ / ⚠️ / ✗] Feature KRs are measurable and business-focused
- [✓ / ⚠️ / ✗] Epics map to exactly one Feature KR each
- [✓ / ⚠️ / ✗] Epic KRs are measurable
- [✓ / ⚠️ / ✗] User Stories map to exactly one Epic each
- [✓ / ⚠️ / ✗] Acceptance criteria map to Epic KRs

**Issues Found:**
- [Issue 1 and recommendation]
- [Issue 2 and recommendation]

---

### ✏️ Recommendations

**High Priority (address before execution):**
1. **[Recommendation 1]** - [Why it's critical]
   - Suggested approach: [How to address]
   - Effort: High / Medium / Low
   - Timeline: [When to address]

2. **[Recommendation 2]** - [Why it's critical]
   - Suggested approach: [How to address]
   - Effort: [Level]
   - Timeline: [When]

**Medium Priority (address before next review cycle):**
1. **[Recommendation 1]** - [Why it's important]
   - Suggested approach: [How to address]
   - Effort: [Level]

2. **[Recommendation 2]** - [Why it's important]
   - Suggested approach: [How to address]
   - Effort: [Level]

**Low Priority (nice to have improvements):**
- [Recommendation 1] - [Why it would improve clarity or completeness]
- [Recommendation 2] - [Why it would help]

---

### 📋 Validation Checklist

Marks from this review:

- [ ] All Strategic Themes have clear business objectives
- [ ] All Features have value hypotheses
- [ ] All Features have 2-4 measurable KRs
- [ ] All Epics map to exactly one Feature KR
- [ ] All Epics have measurable KRs
- [ ] All User Stories have clear acceptance criteria
- [ ] All acceptance criteria map to at least one Epic KR
- [ ] All [Assumption] items are documented
- [ ] All [Open question] items are documented
- [ ] All [Needs validation] items are documented
- [ ] Timeline is realistic (Features: 6-9 months, Epics: ≤3 months)
- [ ] No unresolved dependencies
- [ ] Value flow is traceable from features to business outcomes
- [ ] Decision log is up-to-date and coherent
- [ ] No conflicting decisions documented

---

## Review History

### Previous Review: [Date]

**Reviewer:** [Name/Claude]

**Key Findings:**
- [Finding 1]
- [Finding 2]

**Items Addressed:**
- [✓ Item 1 - Now resolved]
- [✓ Item 2 - Now resolved]

**Items Remaining:**
- [⚠️ Item 1 - Still pending]
- [⚠️ Item 2 - Still pending]

---

### Previous Review: [Date]

[Repeat structure]

---

## Requested Review Topics

When asking Claude to review specific topics, note it here:

### Review Request: [Topic/Document]

**Requested By:** [Name]

**Request Date:** [Date]

**Specific Questions:**
1. [Question 1]
2. [Question 2]
3. [Question 3]

**Review Results:**
- [Finding 1]
- [Finding 2]
- [Recommendation 1]

**Status:** Addressed / Pending / In Progress

---

## Follow-Up Reviews Scheduled

| Topic | Requested By | Reason | Scheduled Date |
|-------|---|---|---|
| [Document/feature] | [Name] | [Why review needed] | [Date] |
| [Document/feature] | [Name] | [Why review needed] | [Date] |

---

## Using Claude for Ongoing Reviews

### Common Review Prompts

**Quick validation of a single feature:**
```
@claude I have a Product Context Pack at [path]. 
Please validate Feature [Name] in 03_requirement_hierarchy.md:
- Does it have a clear value hypothesis?
- Are the Feature KRs measurable and business-focused?
- Do all child Epics map to exactly one Feature KR?
- Are there any gaps or assumptions that need documentation?
```

**Gap analysis across entire pack:**
```
@claude Please review the entire Product Context Pack at [path].
- Find all [Assumption], [Open question], and [Needs validation] items
- Are they distributed across the hierarchy in a way that makes sense?
- What are the highest priority items to resolve before execution?
```

**Hierarchy consistency check:**
```
@claude Please validate the parent-child relationships in 03_requirement_hierarchy.md:
- Does each Feature map properly to its Strategic Theme?
- Does each Epic map to exactly one Feature KR?
- Does each User Story map to one Epic?
- Does each acceptance criterion map to at least one Epic KR?
```

**Value flow validation:**
```
@claude Please trace the value flow in our pack:
- Start with any Feature from 03_requirement_hierarchy.md
- Verify it connects back to business objectives in 01_business_intent.md
- Check if it flows through to metrics in 07_adoption_scorecard.md
- Are there any breaks or unclear connections?
```

---

## Known Issues & Blockers

### Blocker 1: [Issue that prevents execution]

**Description:** [What's blocking]

**Impact:** [How it affects the roadmap]

**Root Cause:** [Why this is blocked]

**Resolution Plan:** [How we'll unblock]

**Owner:** [Who is responsible]

**Target Resolution Date:** [When we expect to unblock]

---

### Issue 2: [Non-blocker issue that should be addressed]

[Repeat structure]

---

## Related Documents

- **Product Context Pack:** See `00_README.md` for navigation
- **Requirements hierarchy:** See `03_requirement_hierarchy.md`
- **Decision log:** See `04_decision_log.md`
- **Claude instructions:** See `CLAUDE.md`
- **Prompt library:** See `10_prompt_library.md`

---

**Last Review Date:** [Date]

**Reviewer:** Claude Haiku (via Copilot)

**Next Scheduled Review:** [Date]

**Review Frequency:** [Every 2 weeks / Monthly / After major changes]
