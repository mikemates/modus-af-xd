# Claude Instructions for This Product Context Pack

Use this file to configure Claude's behavior when analyzing or working with this product context pack.

## System Context

This product context pack contains:
- Strategic themes and features
- Business intent and value flows
- Requirements hierarchy
- Decision logs and learning records
- AI review history

When analyzing this pack, Claude should:

1. **Understand the hierarchy** - Features contain Epics; Epics contain User Stories
2. **Trace value flows** - Connect requirements back to business outcomes
3. **Check consistency** - Ensure each level maps correctly to parent objectives
4. **Identify gaps** - Flag missing assumptions, open questions, unvalidated hypotheses
5. **Use business language** - Frame analysis in terms of revenue, costs, adoption, learning

## How to Reference This Pack

When asking Claude questions about your product:

```
@claude I have a Product Context Pack at [path]. Please analyze [specific file] and [task].
```

Example questions:

- "Are our User Stories properly mapped to Feature KRs?"
- "Where do we have [Open question] or [Assumption] that need validation?"
- "What's the value flow from Feature X to revenue growth?"
- "Which Epics are at risk of missing their Feature KR targets?"
- "Can you extract all decisions from the decision log that affect Feature Y?"

## Claude's Review Focus Areas

When reviewing this pack, Claude should check for:

1. **Alignment** - Do Features connect to Strategic Themes? Do Epics connect to Feature KRs?
2. **Clarity** - Are success criteria measurable? Are assumptions explicit?
3. **Completeness** - Are there gaps in the hierarchy? Missing KRs or acceptance criteria?
4. **Feasibility** - Are timelines realistic (6-9 months for Features, ≤3 months for Epics)?
5. **Value connection** - Can you trace each requirement to a business outcome?

## Using Claude for Analysis

Common workflows:

**Quick Validation**: Ask Claude to validate a single Feature or Epic against the standards

**Gap Analysis**: Ask Claude to find [Assumption], [Open question], and [Needs validation] items

**Hierarchy Check**: Ask Claude to verify parent-child relationships are correct

**Value Mapping**: Ask Claude to trace requirements to business outcomes

**Cohesion**: Ask Claude to identify misalignments between docs (e.g., decision log vs requirements)

## Template for Feedback

When Claude reviews the pack, use this format:

```
## Review of [Document/Section]

### ✓ Strengths
- [What's working well]

### ⚠️ Gaps & Assumptions
- [Explicit unknowns that need resolution]

### 🔄 Alignment Issues
- [Mismatches in the hierarchy or value flow]

### ✏️ Recommendations
- [Specific improvements]
```

## Handoff to Execution

Before exporting requirements to Jira/Linear:

1. Run a full pack review with Claude
2. Address high-priority gaps
3. Confirm all assumptions are documented
4. Validate the value hierarchy
5. Export to `09_backlog_export_ready.md`
6. Have Claude validate the export format

---

Last Updated: [Date]
