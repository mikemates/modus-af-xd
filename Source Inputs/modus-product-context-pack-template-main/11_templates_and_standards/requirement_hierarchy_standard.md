# Requirement Hierarchy Standard

Rules, standards, and validation criteria for the Product Context Pack hierarchy. Use this document to ensure consistency and quality across all requirements.

---

## The Hierarchy

```
Strategic Theme (business investment area, ~12 months)
└─ Feature (6-9 month value-bearing deliverable)
   ├─ Feature KRs (Key Results tied to business outcomes)
   └─ Epic (≤3 month, maps to exactly one Feature KR)
      ├─ Epic KRs (Key Results for this epic)
      └─ User Story (sprint-level, maps to one Epic)
         └─ Acceptance Criteria (observable behaviors)
```

---

## Strategic Theme Standards

### Definition
A Strategic Theme is a major area of business investment over ~12 months. It defines where you're placing resources strategically.

### Requirements

**✓ Must Have:**
- [ ] Clear name (business investment area, not feature name)
- [ ] Explicit business objective (tie to revenue, cost, adoption, learning)
- [ ] Timeline (when this theme spans - e.g., Q1 2024 - Q4 2024)
- [ ] Owner (who is responsible for delivery)
- [ ] 2-4 Features that contribute to this theme
- [ ] Key assumptions documented

**✓ Best Practices:**
- Use business language: "Improve customer retention" not "Build notifications"
- Keep to 2-4 themes per year (more dilutes focus)
- Ensure features in this theme are connected to the same outcome

**✗ Avoid:**
- Theme names that sound like features (e.g., "Mobile App Rewrite")
- Too many themes (causes context switching and partial wins)
- Vague themes without measurable business impact
- Themes without explicit ownership

### Validation Checklist

- [ ] Theme name is outcome-oriented
- [ ] Business objective is clear and measurable
- [ ] Timeline is realistic for 12 months
- [ ] Owner is identified
- [ ] 2-4 Features are mapped to this theme
- [ ] Assumptions are documented

---

## Feature Standards

### Definition
A Feature is a 6-9 month value-bearing deliverable. It directly drives business outcomes. Features are the unit of strategic commitment and should be shippable and measurable.

### Requirements

**✓ Must Have:**
- [ ] Clear name describing the customer value or outcome (not implementation)
- [ ] Value hypothesis: "If we [build this], then [customer value], resulting in [business outcome]"
- [ ] 2-4 measurable Key Results tied to business outcomes (revenue, cost, adoption, learning)
- [ ] One parent Strategic Theme
- [ ] 2-4 Epics that decompose the feature
- [ ] Timeline: 6-9 months
- [ ] Owner (PM and Engineering Lead)
- [ ] Clear scope: what's in and what's explicitly out (v1)
- [ ] Key assumptions and unknowns documented

**✓ Best Practices:**
- Name should describe outcome: "Enable customer self-service booking" not "Build booking system"
- Feature KRs should measure the outcomes promised in the value hypothesis
- Each Epic should map to exactly one Feature KR (not multiple, not zero)
- Include success criteria: "This feature succeeds if [metric] reaches [target] by [date]"
- Document trade-offs: "We're prioritizing [attribute] over [attribute]"

**✗ Avoid:**
- Features without clear value hypothesis
- Too many KRs (pick the top 2-4)
- KRs that measure output not outcome (don't measure "features shipped", measure "revenue impact")
- Features without epics (epics are required for execution planning)
- Vague timelines or unrealistic timelines >12 months

### Feature KR Standards

**Requirements for each Feature KR:**
- [ ] Clear outcome statement (what business impact are we optimizing for?)
- [ ] Measurable target (not "increase revenue" but "increase revenue by $X by Q3")
- [ ] Baseline or current value (so we know if we're moving the needle)
- [ ] Success metric (how we'll measure progress)
- [ ] Owner (who is accountable for this KR)

**Good KR Examples:**
- "Increase bookings per user from 2 to 5 per month (50%+ growth)" - Measurable, specific, outcome-oriented
- "Reduce data entry time from 30 min to 5 min per session" - Clear metric, baseline, target
- "Achieve 40% adoption within target customer segment within 6 months" - Specific, time-bound, outcome-oriented

**Bad KR Examples:**
- "Build the feature" - This is output, not outcome
- "Launch by Q2" - This is a date, not an outcome
- "Improve customer satisfaction" - Too vague, not measurable
- "Increase revenue" - Not enough specificity (by how much? in what segment? by when?)

### Validation Checklist

- [ ] Feature has clear name describing value/outcome
- [ ] Feature has explicit value hypothesis connecting building to business outcome
- [ ] Feature has 2-4 measurable KRs
- [ ] Each KR has target, baseline, success metric, and owner
- [ ] Feature is 6-9 months duration
- [ ] Feature has 2-4 child Epics
- [ ] Each child Epic maps to exactly one Feature KR (no Epic maps to multiple KRs or zero KRs)
- [ ] Feature scope is clear (in-scope and out-of-scope for v1)
- [ ] Owner is identified (PM + Engineering Lead)
- [ ] Key assumptions are documented
- [ ] Open questions are documented

---

## Epic Standards

### Definition
An Epic is a 3-month-or-less deliverable that is part of one Feature and maps to exactly one Feature KR. Epics are how you break Features into execution units.

### Requirements

**✓ Must Have:**
- [ ] Clear name describing the epic's scope
- [ ] Parent Feature (one and only one)
- [ ] Maps to exactly one parent Feature KR (not multiple, not zero)
- [ ] Timeline: ≤3 months (typically 6-8 weeks, one quarter)
- [ ] Owner (Engineering Lead)
- [ ] Scope description (what's delivered, what's not)
- [ ] 2-4 measurable Epic KRs that progress toward the Feature KR
- [ ] 3-8 User Stories that compose the epic
- [ ] Dependencies documented (what must happen first)
- [ ] Key assumptions and unknowns documented

**✓ Best Practices:**
- Name should be specific: "Implement calendar scheduling UI and logic" not "Scheduling epic"
- Each Epic should be independently valuable (could theoretically be released alone)
- Epic KRs should ladder up to Feature KR (e.g., if Feature KR is "50% adoption", Epic KRs might be "35% activation in 8 weeks")
- Have a clear definition of "done" for the epic
- Document what success looks like for engineers

**✗ Avoid:**
- Epics longer than 3 months (breaks into smaller epics)
- Epics that map to multiple Feature KRs (create separate epics)
- Epics without clear User Stories (epics that aren't ready for engineering)
- Too many User Stories in an Epic (>8 stories should be split)
- Epics without dependencies clearly documented

### Epic KR Standards

**Requirements:**
- [ ] Clear outcome statement
- [ ] Measurable target
- [ ] How it contributes to parent Feature KR
- [ ] Success metric

**Good Epic KR Examples:**
- "Achieve 35% activation rate (% of eligible users who use the feature)" - Measurable, specific, contributes to feature KR
- "Reduce time-to-first-use from 20 min to 5 min for new users" - Clear metric and baseline
- "Complete core scheduling workflow with zero errors in testing" - Quality gate, measurable

**Bad Epic KR Examples:**
- "Ship the epic" - This is output, not outcome
- "Implement calendar feature" - Feature name, not outcome
- "Get positive feedback from customers" - Not measurable
- "Increase adoption" - Too vague, needs a specific number and segment

### Validation Checklist

- [ ] Epic has clear name describing scope
- [ ] Epic has exactly one parent Feature
- [ ] Epic maps to exactly one parent Feature KR (verified in Feature)
- [ ] Epic timeline is ≤3 months
- [ ] Epic has 2-4 measurable KRs
- [ ] Epic has 3-8 User Stories
- [ ] Owner is identified (Engineering Lead)
- [ ] Scope is clear (in and out of scope)
- [ ] Dependencies documented
- [ ] Key assumptions documented

---

## User Story Standards

### Definition
A User Story is a sprint-level unit of work that is part of one Epic. User Stories should be completable in 1-2 sprints and have clear acceptance criteria.

### Requirements

**✓ Must Have:**
- [ ] Title/name describing what the story delivers
- [ ] User story in format: "As a [role], I want to [action], so that [value]"
- [ ] Parent Epic (one and only one)
- [ ] 3-5 acceptance criteria that are observable and testable
- [ ] Each acceptance criterion maps to at least one Epic KR
- [ ] Clear scope: what's included, what's not
- [ ] Dependencies documented (what this story depends on)
- [ ] Definition of Done (checklist of what must be true for this story to be "done")
- [ ] Owner/assignee (engineer)
- [ ] Estimated story points (for sprint planning)
- [ ] Assumptions and unknowns documented

**✓ Best Practices:**
- User story format puts user first: "As a [role]" not "As a system"
- Acceptance criteria should be testable by QA without assumptions
- Include "Definition of Done" that includes code review, testing, etc.
- Keep stories to 3-8 story points (if bigger, break into smaller stories)
- Link acceptance criteria to Epic KRs so traceability is clear

**✗ Avoid:**
- Stories that are too small (0-2 points) - combine with another story
- Stories that are too large (>8 points) - break into smaller stories
- Acceptance criteria that are too vague ("must work well")
- Stories without clear value (why are we building this?)
- Acceptance criteria that don't map to KRs

### Acceptance Criteria Standards

Each acceptance criterion must be:
- **Observable:** Can be verified by looking at the product
- **Testable:** Can be tested without ambiguity
- **Valuable:** Contributes to Epic KR and Feature KR
- **Mapped:** Links to at least one Epic KR

**Format:**
```
AC-[N]: [Observable behavior] [Maps to: Epic KR X]
Example: AC-1: Users can filter results by date range within 2 seconds [Maps to: Epic KR 1]
```

**Good Acceptance Criteria:**
- "Users can create a new event by clicking 'New Event' button and filling in required fields" - Observable, testable
- "Form validation shows error message within 1 second of invalid input" - Observable, measurable
- "User can export 10,000+ records in <30 seconds" - Testable performance criterion

**Bad Acceptance Criteria:**
- "The feature should work well" - Not observable
- "Users like the new interface" - Not testable
- "System should be fast" - Not measurable
- "Implement according to designs" - Not a user behavior

### Definition of Done

Each User Story must have a Definition of Done. Example:

- [ ] Code is written and self-reviewed
- [ ] Code is reviewed and approved by team lead
- [ ] Unit tests are written and passing (>80% coverage)
- [ ] Integration tests are passing
- [ ] All acceptance criteria are met
- [ ] QA has tested and approved
- [ ] Product owner has signed off
- [ ] Documentation is updated
- [ ] No critical bugs found

### Validation Checklist

- [ ] Story has clear title
- [ ] Story follows format: "As a [role], I want to [action], so that [value]"
- [ ] Story has exactly one parent Epic
- [ ] Story has 3-5 acceptance criteria
- [ ] Each AC is observable and testable
- [ ] Each AC maps to at least one Epic KR
- [ ] Story has Definition of Done
- [ ] Owner is assigned
- [ ] Story points estimated
- [ ] Dependencies documented
- [ ] Assumptions documented

---

## Mapping & Traceability Rules

### Parent-Child Relationships

**Strategic Theme → Feature:**
- One Strategic Theme can have 2-4 Features
- One Feature has exactly one parent Strategic Theme
- All Features in a Theme should contribute to the Theme's objective

**Feature → Epic:**
- One Feature must have 2-4 Epics
- One Epic has exactly one parent Feature
- Each Epic maps to exactly one Feature KR (all Epics must map, each to a different KR)
- Feature KRs should have at least one Epic working toward them

**Epic → User Story:**
- One Epic should have 3-8 User Stories
- One User Story has exactly one parent Epic
- All User Stories in an Epic should contribute to Epic KRs

**User Story → Acceptance Criteria:**
- One User Story should have 3-5 Acceptance Criteria
- One AC has multiple parent User Stories (can't happen - each AC belongs to exactly one story)
- Each AC must map to at least one Epic KR
- Each Epic KR should have ACs in this Epic mapping to it

### Traceability Validation

To verify traceability:

1. **Top-down:** Pick a Strategic Theme
   - [ ] All Features map to this Theme?
   - [ ] Each Feature has 2-4 Epics?
   - [ ] Each Epic maps to a Feature KR?
   - [ ] Each Epic has 3-8 User Stories?
   - [ ] Each User Story has 3-5 ACs?

2. **Bottom-up:** Pick an Acceptance Criterion
   - [ ] Maps to at least one Epic KR?
   - [ ] Epic KR contributes to Feature KR?
   - [ ] Feature KR contributes to Feature objective?
   - [ ] Feature contributes to Theme objective?

3. **Side-by-side:** Pick a Feature KR
   - [ ] Does at least one Epic map to it?
   - [ ] Do all Epics mapping to it have User Stories?
   - [ ] Do all those User Stories have ACs mapping to the KR?

---

## Marking Unknowns

Throughout the hierarchy, use these labels to mark uncertain information:

**[Assumption]** - Something we're assuming to be true but haven't validated
- Use when: "We assume users will spend 15+ minutes in this feature weekly"
- Implication: This assumption could be wrong; we should validate
- Action: Test, measure, or note as risk

**[Open question]** - Something we don't know and need to answer
- Use when: "How will we detect when this feature is actively used?"
- Implication: We need to answer this before committing resources
- Action: Research, design decision, or customer validation needed

**[Needs validation]** - Something we've decided but need to confirm works
- Use when: "We're targeting 40% adoption by month 3 (needs validation)"
- Implication: We believe this target is realistic, but should track it
- Action: Monitor the metric; adjust if data suggests target is wrong

### Guidelines

- Every Feature should have at least 1-2 [Assumption] or [Open question] items
- Every Epic should have at least 1 [Assumption] or [Needs validation] item
- Be explicit about unknowns (don't hide them in prose)
- Review [Assumption] and [Open question] items monthly
- Update items as they're validated or answered

---

## Quality Checks

### Feature Quality Checklist

```
Feature: [Name]

Value:
  [ ] Has explicit value hypothesis
  [ ] Value hypothesis connects feature to business outcome
  [ ] 2-4 measurable KRs
  [ ] Each KR has baseline and target
  
Scope:
  [ ] Clear in-scope definition
  [ ] Clear out-of-scope definition (what's v2)
  [ ] 6-9 month timeline
  
Execution:
  [ ] 2-4 child Epics
  [ ] Each Epic maps to one Feature KR
  [ ] Owner identified
  [ ] Dependencies documented
  
Quality:
  [ ] Assumptions documented
  [ ] Open questions documented
  [ ] Ready for engineering review
```

### Epic Quality Checklist

```
Epic: [Name]

Alignment:
  [ ] Maps to exactly one Feature KR
  [ ] Has 2-4 measurable KRs
  [ ] KRs contribute to Feature KR
  
Execution:
  [ ] ≤3 months timeline
  [ ] 3-8 User Stories
  [ ] All stories map to one Epic
  [ ] Dependencies documented
  [ ] Owner identified
  
Quality:
  [ ] Assumptions documented
  [ ] Ready for sprint planning
```

### User Story Quality Checklist

```
Story: [Title]

Format:
  [ ] Follows "As a [role], I want to [action], so that [value]"
  [ ] Maps to one Epic
  
Criteria:
  [ ] 3-5 acceptance criteria
  [ ] Each AC is observable
  [ ] Each AC is testable
  [ ] Each AC maps to at least one Epic KR
  
Execution:
  [ ] Definition of Done is complete
  [ ] Assignee identified
  [ ] Story points estimated
  [ ] Dependencies documented
  [ ] Assumptions documented
  [ ] Ready for sprint
```

---

## Maintenance & Updates

### When to Update the Hierarchy

**Update immediately:**
- Feature scope changes
- Timeline changes significantly (±1 month)
- Assumptions are invalidated
- Major discovery changes our direction

**Update in regular cadence:**
- Add User Stories as they're ready for engineering
- Mark User Stories as completed
- Update Epic progress toward KRs
- Mark Epics as complete/shipped

### Keeping It Current

- **Weekly:** Update User Story status and progress
- **Bi-weekly:** Epic KR progress review
- **Monthly:** Feature KR progress, assumptions review
- **Quarterly:** Validate Feature timeline and scope, plan next Epics
- **Quarterly+:** Review Feature KRs and learning; decide continue/change/stop

---

## Common Mistakes to Avoid

| Mistake | Why It's a Problem | How to Fix |
|---------|---|---|
| Feature KRs are outputs, not outcomes | You can't measure business impact | Rewrite to measure business outcome, not activity |
| Epic maps to multiple Feature KRs | Creates ambiguity about what success means | Each Epic maps to exactly one KR |
| User Stories don't link to KRs | Can't verify requirements deliver value | Add AC mapping to Epic KRs |
| Timeline is too aggressive | Features slip and demoralize team | Use 6-9 months for Features, ≤3 for Epics |
| Too many unknowns undocumented | Execution surprises and team confusion | Explicitly mark [Assumption], [Open question], [Needs validation] |
| Hierarchy is never updated | Planning docs diverge from reality | Update status weekly, refresh monthly |

---

## Related Documents

- **Feature template:** See `feature_template.md`
- **Epic template:** See `epic_template.md`
- **User story template:** See `user_story_template.md`
- **Requirements hierarchy:** See `03_requirement_hierarchy.md` (applies these standards)
- **Jira field mapping:** See `jira_field_mapping.md` (exports using these standards)

---

**Standard Version:** 1.0

**Last Updated:** [Date]

**Maintained By:** [Name]

**Review Frequency:** Quarterly

**Questions?** See `10_prompt_library.md` for prompts to validate your hierarchy
