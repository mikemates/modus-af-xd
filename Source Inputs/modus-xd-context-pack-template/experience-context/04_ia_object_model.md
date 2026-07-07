# 04 - IA and Object Model

## Metadata

**Project:** [Project / product name]  
**XD Owner:** [Name]  
**Engineering Contributor:** [Name]  
**Product Owner:** [Name]  
**Status:** Draft / Active / Superseded  
**Last Updated:** [YYYY-MM-DD]  

## Purpose

Define how the product is organized and how users understand, navigate, search, filter, view, and act on product objects.

This file connects user mental models to route structure, data objects, terminology, permissions, and implementation context.

## IA Summary

[2-4 sentences describing the product structure.]

Example:

> The product is organized around [primary object]. Users move from [entry point] to [object list/detail/workflow] to complete [task]. Navigation is shallow/deep because [reason]. The IA must preserve [critical structure] so users can understand where they are and what action is available.

## Navigation Model

**Navigation type:** Global nav / side nav / top nav / wizard / dashboard / object-first / command-driven / other

**Primary navigation rule:** [How users move through the product]

**Secondary navigation rule:** [Tabs, filters, object detail sections, breadcrumbs, etc.]

### Navigation Inventory

| Nav item | Route | Purpose | Visible to | Priority | Notes |
|---|---|---|---|---|---|
| [Label] | [/route] | [Purpose] | [Roles] | P0 / P1 / P2 | [Notes] |

## Route Inventory

| Route ID | Route | Page / screen | Primary object | Primary action | States required | Sandbox link | Story link |
|---|---|---|---|---|---|---|---|
| R-001 | [/route] | [Page] | [Object] | [Action] | Default, empty, loading, error, success | [Link] | [Link] |

## Object Model

### Core Objects

| Object | Definition | User-facing term | System/API term | Owner | Notes |
|---|---|---|---|---|---|
| [Object] | [Definition] | [Term] | [Term] | [Owner] | [Notes] |

### Object Relationships

| Object A | Relationship | Object B | Cardinality | User implication | Implementation note |
|---|---|---|---|---|---|
| [Object] | has / belongs to / creates / approves / contains | [Object] | 1:1 / 1:many / many:many | [Implication] | [Note] |

### Object States

| Object | State | Definition | User-visible label | Allowed actions | Next states |
|---|---|---|---|---|---|
| [Object] | [State] | [Definition] | [Label] | [Actions] | [States] |

## Content Hierarchy

| Page / route | Primary content | Secondary content | Actions | Empty-state content | Notes |
|---|---|---|---|---|---|
| [Page] | [Content] | [Content] | [Actions] | [Content] | [Notes] |

## Terminology Rules

| Concept | Approved term | Avoid | Rationale |
|---|---|---|---|
| [Concept] | [Term] | [Term to avoid] | [Reason] |

## Permissions and Visibility Rules

| Role | Route / object | Can view | Can act | Hidden or disabled? | Notes |
|---|---|---:|---:|---|---|
| [Role] | [Route/object] | Yes / No | Yes / No | Hidden / disabled / visible read-only | [Notes] |

## Search, Filter, and Sort

| Object/list | Search fields | Filters | Sort options | Default sort | Notes |
|---|---|---|---|---|---|
| [List] | [Fields] | [Filters] | [Sort] | [Default] | [Notes] |

## Responsive and Layout Implications

| Route / component | Desktop behavior | Tablet behavior | Mobile behavior | Risk |
|---|---|---|---|---|
| [Route] | [Behavior] | [Behavior] | [Behavior] | [Risk] |

## IA Decisions

| Decision | Rationale | Alternatives considered | Decision log link |
|---|---|---|---|
| [Decision] | [Why] | [Alternatives] | [Link] |

## Assumptions and Open Questions

- **[Assumption]** [Statement]
- **[Open question]** [Question]
- **[Needs validation]** [Validation item]

## Agent Guidance

When generating routes, UI, or test cases:

- Use route IDs and object names exactly as defined.
- Do not invent new objects, states, or terms without updating this file.
- Respect role-based visibility rules.
- Preserve approved navigation labels unless a decision log entry changes them.

## Quality Standard

This file is ready when a new team member or AI agent can understand the product's route structure, core objects, relationships, terminology, and visibility rules without relying on verbal explanation.

## Related Documents

- Users, Tasks, Roles: `02_users_tasks_roles.md`
- Journeys and Flows: `03_journeys_flows.md`
- Sandbox Manifest: `05_sandbox_manifest.md`
- Content and Language: `08_content_language.md`
