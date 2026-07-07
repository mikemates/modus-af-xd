# Prompt Library

Reusable Claude prompts for analyzing and working with the Product Context Pack. Copy and customize these for your specific context.

---

## Quick Reference: Most Common Prompts

**Validate a Feature:**
```
@claude I have a Product Context Pack at [path]. 
Please validate Feature [Name] in 03_requirement_hierarchy.md.
Check: value hypothesis, measurable KRs, child epics map to one KR each, realistic timeline.
Flag any gaps or assumptions needing documentation.
```

**Review entire pack for gaps:**
```
@claude Please review the entire Product Context Pack at [path].
Find all [Assumption], [Open question], and [Needs validation] items.
Group them by document. What are the top 3 priorities to resolve?
```

**Check hierarchy consistency:**
```
@claude Please validate parent-child relationships in 03_requirement_hierarchy.md at [path]:
- Features → Strategic Themes: correct mapping?
- Epics → Features: each Epic maps to exactly one Feature KR?
- User Stories → Epics: one story per epic?
- Acceptance Criteria → Epic KRs: each AC maps to at least one KR?
```

**Analyze value flow:**
```
@claude Please trace the value flow in the Product Context Pack at [path].
Pick any Feature from 03_requirement_hierarchy.md.
Show how it connects to business outcomes in 01_business_intent.md.
Verify it flows to metrics in 07_adoption_scorecard.md.
Any breaks or unclear connections?
```

---

## Detailed Prompt Library

### 1. Strategic Planning & Analysis

#### 1.1 Validate Business Intent

**Purpose:** Check that the business problem, opportunity, and success criteria are clear

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please review 01_business_intent.md and answer:
1. Is the business problem clearly stated (customer pain point)?
2. Are business objectives specific and measurable?
3. Are success criteria tied to metrics you can track?
4. Are the key assumptions and unknowns documented?
5. Are there any gaps that could derail execution?

Format as: [✓ Strength] / [⚠️ Gap] / [✗ Critical Issue]
```

**When to use:** Starting a new initiative, reviewing with leadership, before committing resources

---

#### 1.2 Analyze Value Flow

**Purpose:** Verify that features actually drive business outcomes

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please analyze the value flow in 02_value_flow_map.md:
1. For each major feature, trace: Feature → Customer Value → Business Outcome
2. Identify any weak links (e.g., customer value doesn't lead to outcomes)
3. Check if metrics in 07_adoption_scorecard.md actually measure this value
4. What assumptions are we making about customer adoption and willingness to pay?
5. What risks could break the value chain?

Show the full chain for each key feature.
```

**When to use:** Quarterly strategy review, before major feature launches, investor presentations

---

#### 1.3 Challenge Assumptions

**Purpose:** Surface untested assumptions that could cause failure

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please find and categorize all assumptions in the pack:
1. Find all [Assumption] items
2. For each one, assess: 
   - How critical is this assumption to success? (Critical / Important / Nice to validate)
   - How confident are we? (High / Medium / Low)
   - How would we know if it's wrong?
3. What's the top 3 assumptions we MUST validate before scaling?
4. What experiments or data would validate them?

Create a prioritized action plan.
```

**When to use:** Risk analysis, before major resource commitments, after failed predictions

---

### 2. Requirements & Hierarchy

#### 2.1 Validate Feature Completeness

**Purpose:** Ensure a Feature has everything needed to guide development

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please validate Feature [FEATURE_NAME] in 03_requirement_hierarchy.md:

✓ Completeness check:
  - Does it have a clear value hypothesis?
  - Does it have 2-4 measurable KRs? (Not 10, not 1)
  - Do the KRs tie to business outcomes from 01_business_intent.md?
  - Are all child Epics documented?
  - Does each Epic map to exactly one Feature KR?
  - Is the timeline realistic (6-9 months)?

⚠️ Clarity check:
  - Could an engineer read this and start building?
  - Are dependencies clear?
  - Are assumptions documented?

Report: [Status], [Strengths], [Gaps], [Recommendations]
```

**When to use:** Before starting a feature, quarterly review, new PM onboarding

---

#### 2.2 Validate Epic Completeness

**Purpose:** Ensure an Epic is ready for sprint planning

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please validate Epic [EPIC_NAME] in 03_requirement_hierarchy.md:

✓ Quality check:
  - Clear scope (what's in, what's out)?
  - Maps to exactly one Feature KR?
  - Has 2-3 measurable KRs?
  - User Stories are detailed?
  - All acceptance criteria present?
  - Timeline is ≤3 months?
  - Dependencies documented?

⚠️ Readiness check:
  - Is this ready for engineering to start sprinting?
  - Are there any blockers?
  - Any assumptions that need validation first?

Report status and blockers.
```

**When to use:** Sprint planning, epic kickoff, before marking as "Ready"

---

#### 2.3 Validate User Story Completeness

**Purpose:** Ensure a User Story meets acceptance criteria for inclusion in sprints

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please validate User Story [STORY_ID] in 03_requirement_hierarchy.md:

✓ Standards check:
  - Follows "As a [role], I want to [action], so that [value]" format?
  - Has 3-5 acceptance criteria?
  - Each AC is observable and testable?
  - Each AC maps to at least one Epic KR?
  - Definition of Done is complete?

⚠️ Clarity check:
  - Could a developer start coding without questions?
  - Are dependencies clear?
  - Is the scope right for one sprint?

✗ Issues found:
  - [Issue 1]
  - [Issue 2]

Recommendations: [How to fix]
```

**When to use:** Story refinement, before adding to sprint, before assigning to engineer

---

#### 2.4 Check Hierarchy Consistency

**Purpose:** Validate that parent-child relationships are correct throughout the hierarchy

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please check all parent-child relationships in 03_requirement_hierarchy.md:

For each level:
1. Features → Strategic Themes: Do all Features connect to themes? (Should be 1:many)
2. Epics → Features: Does each Epic map to exactly one Feature KR?
3. User Stories → Epics: Does each Story belong to one Epic?
4. Acceptance Criteria → Epic KRs: Does each AC map to at least one KR?

Report:
- [✓] Relationships that are correct
- [⚠️] Relationships that are unclear
- [✗] Broken relationships

For any issues, suggest how to fix.
```

**When to use:** Pack validation, before exporting to Jira, quarterly review

---

### 3. Decisions & Trade-offs

#### 3.1 Validate Decision Log

**Purpose:** Ensure decisions are well-documented and coherent

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please review the decision log (04_decision_log.md) and answer:
1. Are major decisions documented (strategic, product, technical)?
2. For each decision:
   - Is the rationale clear?
   - Are alternatives considered?
   - Are assumptions documented?
   - Does it connect to the roadmap?
3. Are there conflicts or contradictions between decisions?
4. What decisions are missing that should be documented?

Report: [Decision quality], [Conflicts], [Missing decisions]
```

**When to use:** Monthly review, onboarding engineers, new PM orientation

---

#### 3.2 Analyze a Specific Decision

**Purpose:** Understand the reasoning behind a significant choice

**Prompt:**
```
@claude I have a Product Context Pack at [path].

I'm trying to understand decision [DECISION_ID] in 04_decision_log.md.

Please explain:
1. What problem was this decision solving?
2. What alternatives were considered?
3. Why was this option selected?
4. What's the risk if this decision is wrong?
5. How would we know if we should reverse it?
6. What does this decision enable or constrain in the roadmap?

Help me understand the trade-offs.
```

**When to use:** New team member learning, reconsidering a past decision, understanding constraints

---

### 4. Learning & Iteration

#### 4.1 Analyze Release Outcomes

**Purpose:** Extract insights from a completed release

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please review Release [RELEASE_ID] in 06_release_learning_map.md:

1. What did we expect to happen? (hypotheses and targets)
2. What actually happened? (metrics and outcomes)
3. What surprised us (positive or negative)?
4. What assumptions did we validate or invalidate?
5. What should we continue, change, or stop doing?
6. How does this change what we build next?

Report: [Key learnings], [Continue/Change/Stop decisions], [Roadmap implications]
```

**When to use:** Post-release retrospectives, quarterly planning, identifying trends

---

#### 4.2 Identify Patterns Across Releases

**Purpose:** Find meta-patterns that inform strategy

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please review all releases in 06_release_learning_map.md and find patterns:

1. What customer behaviors appear consistently across releases?
2. What assumptions have we validated or invalidated repeatedly?
3. Are there recurring adoption challenges?
4. What's working? What keeps failing?
5. How is our forecast accuracy? Are we over/underestimating?
6. What's changing in customer demand or behavior?

Report: [Patterns found], [Strategic implications], [Recommendations]
```

**When to use:** Annual planning, strategy pivots, investor updates

---

### 5. Adoption & Metrics

#### 5.1 Validate Adoption Strategy

**Purpose:** Check that adoption metrics are aligned with business goals

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please review the adoption scorecard (07_adoption_scorecard.md):

1. Are leading indicators predictive of lagging indicators?
2. Do we have enough leading indicators to spot problems early?
3. Are targets realistic based on historical data?
4. Do metrics align with business objectives from 01_business_intent.md?
5. Are we measuring the right segments?
6. What metrics are we missing?

Report: [Scorecard quality], [Gaps], [Recommendations]
```

**When to use:** Monthly review, quarterly planning, strategy validation

---

#### 5.2 Identify Adoption Blockers

**Purpose:** Find why a feature isn't being adopted

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Feature [FEATURE_NAME] is not reaching adoption targets in 07_adoption_scorecard.md.

Based on the product context pack:
1. What was the value hypothesis for this feature?
2. What were the adoption targets and success criteria?
3. What could explain the gap? (Look at: value fit, UX, pricing, market timing, competition, etc.)
4. What data or customer feedback would help diagnose the real issue?
5. What are possible interventions? (product changes, positioning, go-to-market, etc.)

Report: [Likely causes], [Diagnostic questions], [Possible solutions]
```

**When to use:** Feature underperforming, quarterly adoption review, retro analysis

---

### 6. Export & Integration

#### 6.1 Validate Jira/Linear Export

**Purpose:** Ensure the backlog is properly formatted for import

**Prompt:**
```
@claude I have a Product Context Pack at [path].

I'm about to export requirements to [Jira/Linear] using 09_backlog_export_ready.md.

Please check:
1. Are all parent-child relationships correct?
2. Are all required fields populated?
3. Do all status values match [Jira/Linear] options?
4. Are there any missing IDs or duplicates?
5. Will the import work without errors?

Report: [Validation status], [Errors], [Warnings], [OK to export?]
```

**When to use:** Before major Jira/Linear imports, new team member training, quality gate

---

#### 6.2 Generate Backlog Summary for Team

**Purpose:** Create a brief overview of what's being built

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please create a brief backlog summary from 03_requirement_hierarchy.md and 09_backlog_export_ready.md:

1. What are the top Strategic Themes we're investing in?
2. For each Theme, what are the Features?
3. What's the delivery timeline?
4. What's the expected business impact?
5. What are the top 3 things we're NOT doing (out of scope)?

Format as: 1-page executive summary suitable for team standup.
```

**When to use:** Weekly team update, new stakeholder onboarding, all-hands briefing

---

### 7. AI Review & Quality

#### 7.1 Full Pack Validation

**Purpose:** Comprehensive quality check of the entire pack

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please do a comprehensive review:

✓ COMPLETENESS:
  - Is 01_business_intent.md complete?
  - Is 02_value_flow_map.md complete?
  - Is 03_requirement_hierarchy.md complete and detailed?
  - Are decisions in 04_decision_log.md documented?

⚠️ ALIGNMENT:
  - Do Features connect to business objectives?
  - Does value flow from features to outcomes?
  - Are metrics aligned with business goals?

🔄 CONSISTENCY:
  - Do hierarchy relationships work?
  - Are there conflicting decisions?
  - Do metrics in scorecard match value flow?

✏️ RECOMMENDATIONS:
  - Top 3 gaps to address?
  - Top 3 improvements to make?
  - Is this ready for execution?

Report format: [Strengths] | [Gaps] | [Recommendations]
```

**When to use:** Quarterly review, pre-launch validation, stakeholder presentations

---

#### 7.2 Generate AI Review Notes Document

**Purpose:** Create an official review that goes into 08_ai_review_notes.md

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please create a formal AI review that I can save into 08_ai_review_notes.md.

Include:
1. Strengths (2-3 areas doing well)
2. Gaps & Unknowns (list all [Assumption], [Open question], [Needs validation])
3. Alignment Issues (hierarchy, value flow, consistency)
4. Recommendations (priority-ordered with effort estimate)
5. Validation Checklist (mark each item ✓/⚠️/✗)

Use the format from 08_ai_review_notes.md template.
```

**When to use:** Monthly reviews, sharing feedback with team, documenting quality gates

---

### 8. Troubleshooting & Edge Cases

#### 8.1 Debug Why a Feature Isn't Clear

**Purpose:** Fix a feature that's too vague for engineering to start

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Feature [FEATURE_NAME] in 03_requirement_hierarchy.md is too vague. Engineering has questions.

Please help clarify:
1. What is the core customer value being delivered?
2. What problem are we solving that's different from [competitor/current state]?
3. What are the non-negotiable elements?
4. What can vary based on what we learn?
5. What would "success" look like for an engineer implementing this?
6. What are the key assumptions we're betting on?

Generate: [Clear scope definition], [Success criteria], [Key assumptions]
```

**When to use:** Feature kickoff, engineer questions, requirements clarification

---

#### 8.2 Identify Hidden Dependencies

**Purpose:** Find dependency chains that could block execution

**Prompt:**
```
@claude I have a Product Context Pack at [path].

Please analyze 03_requirement_hierarchy.md for hidden dependencies:

1. What Epics depend on other Epics?
2. What infrastructure or data setup is needed before certain stories can start?
3. Are there Epics that must ship in a specific order?
4. What could cause the critical path to slip?
5. How could we parallelize work to reduce timeline?

Report: [Dependency map], [Critical path], [Parallelization opportunities]
```

**When to use:** Roadmap planning, timeline optimization, risk mitigation

---

---

## Tips for Best Results

**Be Specific:**
- Reference specific documents and section names
- Provide the actual path to your pack
- Be clear about what you're trying to accomplish

**Provide Context:**
- Include relevant background (timeline, market, constraints)
- Point Claude to related documents for cross-reference
- Mention what you've already tried

**Ask for Structure:**
- Request specific formats (tables, lists, summaries)
- Ask for priority ordering
- Request actionable recommendations

**Iterate:**
- Ask follow-up questions if the answer isn't clear
- Ask Claude to explain the reasoning
- Build on previous analyses

---

## Related Documents

- **Full Product Context Pack:** See `00_README.md` for navigation
- **Claude instructions:** See `CLAUDE.md` for system setup
- **AI review notes:** See `08_ai_review_notes.md` for review history

---

**Prompt Library Version:** 1.0

**Last Updated:** [Date]

**Contributor:** [Names]
