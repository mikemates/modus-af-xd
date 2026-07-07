# Product Context Pack Template

This repository contains a reusable template for organizing product strategy, requirements, and decision-making artifacts in a structured format. It's designed to be version-controlled and easily navigable for teams using Claude, Jira, or other planning tools.

## Quick Start

1. **Copy this repository** as the basis for a new client engagement or product initiative
2. **Follow the numbering sequence** (00_, 01_, etc.) through the planning documents
3. **Use the templates** in `11_templates_and_standards/` to maintain consistency
4. **Keep `05_living_specs/`** updated throughout the product lifecycle

## Document Structure

### Strategy & Context
- `00_README.md` - Navigation guide for this pack
- `01_business_intent.md` - Business problem, market context, success criteria
- `02_value_flow_map.md` - How value flows from features to business outcomes
- `03_requirement_hierarchy.md` - Strategic Themes → Features → Epics → User Stories

### Decision & Learning
- `04_decision_log.md` - Architecture, product, and strategic decisions
- `06_release_learning_map.md` - Releases, outcomes, and lessons learned
- `07_adoption_scorecard.md` - Leading and lagging adoption indicators

### Quality & Integration
- `08_ai_review_notes.md` - Claude/AI feedback and review summaries
- `09_backlog_export_ready.md` - Jira/Linear import-ready format
- `10_prompt_library.md` - Reusable prompts for Claude and other tools

### Source Inputs
- `00_source_inputs/` - Client research, competitive analysis, industry context

### Standards
- `11_templates_and_standards/` - Templates and standards for all work products

## Template Hierarchy

```
Strategic Theme (business investment area)
├── Feature (6-9 month value-bearing deliverable)
│   ├── Feature KRs (Key Results tied to business outcomes)
│   └── Epic (≤3 month, one Feature KR per Epic)
│       ├── Epic KRs
│       └── User Story (sprint-level)
│           └── Acceptance criteria (map to Epic KRs)
```

## How to Use

1. **Start with business intent** - Document the problem in `01_business_intent.md`
2. **Map value flow** - Use `02_value_flow_map.md` to trace revenue/cost/adoption impact
3. **Populate requirements** - Build hierarchy in `03_requirement_hierarchy.md`
4. **Document decisions** - Record rationale in `04_decision_log.md`
5. **Track learning** - Update `06_release_learning_map.md` each release
6. **Review with AI** - Get feedback in `08_ai_review_notes.md`
7. **Export for execution** - Format for `09_backlog_export_ready.md`

## Key Rules

- Each Feature has a **value hypothesis** and **Feature KRs**
- Each Epic maps to **exactly one parent Feature KR**
- Each User Story acceptance criterion maps to **at least one Epic KR**
- Use **business language**: revenue growth, operating cost, adoption, learning signals
- Mark unknowns as **[Assumption]**, **[Open question]**, or **[Needs validation]**

## Maintenance

- Keep documents in sync with execution
- Use decision log to record why changes were made
- Capture learning after each release
- Review adoption metrics monthly
- Refresh with AI every 2-4 weeks

---

Generated from the Modus Product Context Pack Template
