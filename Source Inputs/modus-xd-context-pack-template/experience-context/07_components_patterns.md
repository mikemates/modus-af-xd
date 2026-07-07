# 07 - Components and Patterns

## Metadata

**Project:** [Project / product name]  
**XD Owner:** [Name]  
**Engineering Contributor:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  

## Purpose

Define the UI foundation, component library, reusable patterns, system constraints, and known component gaps for the product.

This file helps engineers and agents avoid inventing UI patterns when approved components or conventions already exist.

## UI Foundation Summary

**Design system source:** [None / client design system / Modus starter / component library / hybrid]

**Component library:** [Name and version]

**Theme/token source:** [Name/path]

**Figma source:** [Link, if required]

**Sandbox source:** [Link]

**Production source:** [Link, if available]

## Component Strategy

| Category | Strategy | Notes |
|---|---|---|
| Existing approved components | Use as-is / adapt / avoid | [Notes] |
| Component library defaults | Use as-is / theme / wrap | [Notes] |
| Custom components | Allowed / discouraged / requires review | [Notes] |
| New patterns | Allowed with review / not allowed | [Notes] |
| Figma parity | Required / selective / not required | [Notes] |

## Approved Components

| Component | Source | Use for | Variants/states | Accessibility notes | Sandbox example |
|---|---|---|---|---|---|
| [Component] | [Library/system] | [Use case] | [Variants] | [Notes] | [Route/link] |

## Customized Components

| Component | Source | Customization | Why needed | Production review needed | Status |
|---|---|---|---|---|---|
| [Component] | [Source] | [Change] | [Reason] | Yes / No | Draft / Approved |

## New Components Required

| Component | Use case | Why existing components do not fit | Owner | Decision needed |
|---|---|---|---|---|
| [Component] | [Use case] | [Reason] | [Owner] | [Decision] |

## Layout Conventions

| Pattern | Rule | Example | Notes |
|---|---|---|---|
| Page shell | [Rule] | [Route] | [Notes] |
| List/detail | [Rule] | [Route] | [Notes] |
| Dashboard cards | [Rule] | [Route] | [Notes] |
| Wizard/stepper | [Rule] | [Route] | [Notes] |
| Form layout | [Rule] | [Route] | [Notes] |

## Form Patterns

| Form pattern | Use when | Required behavior | Component(s) | Notes |
|---|---|---|---|---|
| [Pattern] | [Use case] | [Behavior] | [Components] | [Notes] |

## Data Display Patterns

| Pattern | Use when | Sorting/filtering | Empty/error behavior | Notes |
|---|---|---|---|---|
| Table | [Use case] | [Rules] | [Behavior] | [Notes] |
| Card list | [Use case] | [Rules] | [Behavior] | [Notes] |
| Detail panel | [Use case] | [Rules] | [Behavior] | [Notes] |

## Feedback and Status Patterns

| Pattern | Use when | Component | Copy source | Notes |
|---|---|---|---|---|
| Toast | [Use case] | [Component] | [Source] | [Notes] |
| Inline alert | [Use case] | [Component] | [Source] | [Notes] |
| Badge/status tag | [Use case] | [Component] | [Source] | [Notes] |

## Modals, Drawers, and Popovers

| Pattern | Use when | Avoid when | Accessibility requirement | Notes |
|---|---|---|---|---|
| Modal | [Use case] | [Avoid] | [Requirement] | [Notes] |
| Drawer | [Use case] | [Avoid] | [Requirement] | [Notes] |
| Popover | [Use case] | [Avoid] | [Requirement] | [Notes] |

## Token and Styling Guidance

| Token area | Source | Rule | Notes |
|---|---|---|---|
| Color | [Source] | [Rule] | [Notes] |
| Typography | [Source] | [Rule] | [Notes] |
| Spacing | [Source] | [Rule] | [Notes] |
| Radius | [Source] | [Rule] | [Notes] |
| Elevation | [Source] | [Rule] | [Notes] |

## Known Component Gaps

| Gap | Impact | Workaround | Decision needed | Owner |
|---|---|---|---|---|
| [Gap] | [Impact] | [Workaround] | [Decision] | [Owner] |

## Design Debt

| Debt item | Reason accepted | Risk | Follow-up story | Owner |
|---|---|---|---|---|
| [Debt] | [Reason] | [Risk] | [Link] | [Owner] |

## Agent Guidance

- Use named components and patterns from this file.
- Do not create custom UI if an approved component exists.
- If a component does not support a required state, mark a component gap.
- Preserve accessibility requirements attached to components.
- Treat sandbox component code as reference-only unless engineering approves reuse.

## Quality Standard

This file is ready when stories and agents can identify approved components, layout conventions, pattern rules, component gaps, and system constraints without inventing new UI decisions.

## Related Documents

- IA and Object Model: `04_ia_object_model.md`
- Sandbox Manifest: `05_sandbox_manifest.md`
- Interaction States: `06_interaction_states.md`
- Accessibility and Usability: `09_accessibility_usability.md`
