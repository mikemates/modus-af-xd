# Experience Sandbox

This folder defines the recommended documentation model for a design-authored Experience Sandbox.

The actual sandbox may live in a separate repository, subrepo, or isolated app folder. This folder provides the handoff and governance files that should travel with the sandbox.

## Purpose

The Experience Sandbox is a coded mock/prototype environment created by XD to demonstrate product experience intent using routes, flows, states, interaction behavior, representative data, and component patterns.

It is not production software. It is implementation context.

## Sandbox Metadata

**Product / project:** [Name]

**Sandbox repo:** [URL]

**Preview URL:** [URL]

**Primary owner:** [XD owner]

**Engineering reviewer:** [Engineering lead]

**Component library:** [Name]

**Runtime / stack:** [React, Next, Vite, etc.]

**Status:** Draft / In Review / Approved for Backlog / Archived

## What This Sandbox Should Include

- Primary user flows
- Core routes/screens
- Navigation model
- Representative mock data
- Default, loading, empty, error, and success states where relevant
- Important form behavior and validation
- Role or permission distinctions where relevant
- Interaction patterns that matter for implementation
- Content and terminology examples
- Accessibility intent where feasible

## What This Sandbox Should Not Be

- Production-ready code
- A replacement for architecture
- A replacement for product backlog
- A bypass around engineering review
- A complete application
- A source of truth that drifts without governance

## Recommended Folder Pattern

```text
experience-sandbox/
  README.md        (this file: setup, code hygiene, how eng/agents use it)
  drift_log.md     (sandbox-vs-production drift, updated during build)

app-or-src/
  routes-or-pages/
  components/
  data/
  styles-or-theme/
  docs/
```

Route/flow/state coverage, mock-data coverage, and reusable-vs-reference mapping live in the manifest (`../experience-context/05_sandbox_manifest.md`), not in this folder — one source, no duplication.

## Local Setup Placeholder

```bash
[install command]
[run command]
[test command]
```

## Code Hygiene Expectations

Sandbox code does not need to meet production engineering standards, but it should be useful enough for engineering and agents to inspect.

Minimum expectations:

- Clear route and file names
- Simple component boundaries
- Mock data separated from UI where practical
- No production secrets
- No client-confidential data unless approved
- Comments where behavior is intentionally simplified
- Reference-only areas marked clearly
- No misleading production-readiness claims

## Required Handoff Files

- `../experience-context/05_sandbox_manifest.md` — the mapping of routes/states/data to flows and backlog, and what is reusable vs. reference-only
- `drift_log.md` — differences between sandbox and production, captured during build

## How Engineering and Agents Should Use This Sandbox

Use the sandbox to understand intended flow, route/navigation structure, interaction behavior, state coverage, content direction, component assumptions, and representative data.

Do **not** use it as production architecture, a final code-quality standard, a source of auth/authorization/API implementation, or a replacement for backlog acceptance criteria.

Before treating the sandbox as backlog input, confirm via the Sandbox Review gate in `../templates-and-standards/experience_quality_review.md` that the manifest is current, states are covered or documented as missing, reusable vs. reference-only elements are marked, open questions are visible, and Engineering/QE have reviewed feasibility and testability.

## Quality Standard

The sandbox is ready for backlog input when Product, XD, Engineering, QE, and agents can understand the intended experience, route/state coverage, implementation relevance, and known gaps without a live walkthrough.
