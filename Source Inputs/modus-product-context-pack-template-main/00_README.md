# Product Context Pack Navigation Guide

Welcome to the Product Context Pack. This guide will help you navigate and use all the documents effectively.

## Document Navigation Map

```
START HERE: 01_business_intent.md
    ↓
02_value_flow_map.md (understand value delivery)
    ↓
03_requirement_hierarchy.md (build requirements)
    ↓
05_living_specs/ (detailed specifications)
    ↓
04_decision_log.md (record key decisions)
    ↓
09_backlog_export_ready.md (ready for execution tools)
    ↓
06_release_learning_map.md (capture outcomes)
```

## Document Purposes

### Phase 1: Discovery & Strategy

**01_business_intent.md**
- What problem are we solving?
- Who is the customer?
- What's the business opportunity?
- How will we know if we're successful?

**02_value_flow_map.md**
- How do features create customer value?
- How does customer value translate to business outcomes?
- What are the key assumptions in this model?

### Phase 2: Planning

**03_requirement_hierarchy.md**
- Strategic Themes (business investment areas)
- Features (6-9 month value-bearing deliverables)
- Epics (≤3 month milestones)
- User Stories (sprint-level work)

**00_source_inputs/** (research & context)
- `00_source_inventory.md` - What source material informed this pack
- `client_analysis_template.md` - Customer needs, pain points, context
- `competitor_analysis_template.md` - Market alternatives, differentiation
- `industry_analysis_template.md` - Trends, regulations, opportunities

### Phase 3: Execution Planning

**04_decision_log.md**
- Key product decisions and rationale
- Architecture decisions
- Strategic trade-offs
- Why certain options were selected or rejected

**09_backlog_export_ready.md**
- Jira/Linear ready format
- All requirements, epics, user stories
- Field mapping and metadata
- Import-ready structure

**10_prompt_library.md**
- Reusable Claude prompts for common tasks
- Questions that unlock thinking
- Analysis templates
- Handoff instructions

### Phase 4: Learning & Iteration

**06_release_learning_map.md**
- What we built and when
- What we learned
- What changed (continue/change/stop decisions)
- Metrics and outcomes

**07_adoption_scorecard.md**
- Leading indicators (usage, engagement)
- Lagging indicators (revenue, costs, customer satisfaction)
- Adoption targets by segment
- Progress tracking

**08_ai_review_notes.md**
- Claude reviews and feedback
- Validation results
- Recommended improvements
- Unresolved questions

## Quick Reference: Templates

All templates are in `11_templates_and_standards/`:

- `feature_template.md` - Use for every Feature
- `epic_template.md` - Use for every Epic
- `user_story_template.md` - Use for every User Story
- `requirement_hierarchy_standard.md` - Rules for parent-child relationships
- `jira_field_mapping.md` - Map requirements to Jira/Linear fields

## The Hierarchy at a Glance

```
Strategic Theme
  └─ Feature (value hypothesis + Feature KRs)
       └─ Epic (≤3 months, maps to 1 Feature KR)
            └─ User Story (sprint-level)
                 └─ Acceptance criteria (map to Epic KRs)
```

### Key Rules

1. **One Feature** = 6-9 months of focused work
2. **One Epic** = ≤3 months, part of one Feature, maps to exactly one Feature KR
3. **One User Story** = 1-2 sprints, part of one Epic
4. **One Acceptance Criterion** = maps to at least one Epic KR

## Using This Pack

### For Product Managers
- Start with 01_business_intent.md
- Maintain 03_requirement_hierarchy.md
- Update 06_release_learning_map.md after each release
- Keep 04_decision_log.md current

### For Engineers
- Reference 09_backlog_export_ready.md
- Check 04_decision_log.md for architecture context
- Use 05_living_specs/ for detailed specifications
- Reference 10_prompt_library.md for Claude prompts

### For Stakeholders
- Read 01_business_intent.md for context
- Check 07_adoption_scorecard.md for progress
- Review 06_release_learning_map.md for outcomes
- Ask questions documented in 08_ai_review_notes.md

### For AI Analysis
- Use CLAUDE.md for system instructions
- Reference 10_prompt_library.md for analysis tasks
- Check 08_ai_review_notes.md for prior feedback
- Review entire pack for consistency checks

## Marking Unknowns

Throughout the pack, mark uncertain information:

- **[Assumption]** - Something we're assuming to be true but haven't validated
- **[Open question]** - Something we don't know and need to answer
- **[Needs validation]** - Something we've decided but need to confirm works

Example:
> User Story: "As a [user], I want to [action] so that [value]"
> 
> [Assumption] Users spend 15+ minutes in this workflow weekly
> [Open question] How will we detect when this feature is actively used?
> [Needs validation] Target adoption rate of 60% by month 3

## Maintenance Schedule

| Task | Frequency | Owner |
|------|-----------|-------|
| Update 03_requirement_hierarchy.md | Every 2 weeks | Product Manager |
| Update 04_decision_log.md | After each decision | Product/Engineering |
| Update 06_release_learning_map.md | After each release | Product Manager |
| Update 07_adoption_scorecard.md | Monthly | Analytics/Product |
| AI review (08_ai_review_notes.md) | Every 2-4 weeks | Product Manager + Claude |

## Exporting to Execution Tools

When ready to export to Jira/Linear:

1. Ensure 03_requirement_hierarchy.md is complete and validated
2. Run through templates in 11_templates_and_standards/
3. Get AI review in 08_ai_review_notes.md
4. Format for export in 09_backlog_export_ready.md
5. Use 11_templates_and_standards/jira_field_mapping.md to map fields

---

**How to Get Help:**
- Check CLAUDE.md for how to use Claude with this pack
- See 10_prompt_library.md for common analysis tasks
- Review 08_ai_review_notes.md for prior feedback on questions

**Pack Version:** 1.0
**Last Updated:** [Date]
