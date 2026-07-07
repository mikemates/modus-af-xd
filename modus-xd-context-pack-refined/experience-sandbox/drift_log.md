# Sandbox Drift Log

## Purpose

Track differences between the Experience Sandbox and production implementation.

Drift is expected. Undocumented drift creates confusion, weakens agent context, and makes future backlog work less reliable.

## Drift Log

| Drift ID | Date | Area | Sandbox behavior | Production behavior | Reason | Decision | Owner | Follow-up |
|---|---|---|---|---|---|---|---|---|
| D-001 | [Date] | [Area] | [Sandbox] | [Production] | [Reason] | Accepted / Fix sandbox / Fix production / Add backlog | [Owner] | [Link] |

## Drift Categories

| Category | Definition | Example |
|---|---|---|
| Intentional implementation change | Engineering changed behavior for technical, architecture, or feasibility reasons | [Example] |
| Experience debt | Production does not yet meet intended experience | [Example] |
| Sandbox outdated | Sandbox no longer reflects decided product direction | [Example] |
| Pattern improvement | Production improved beyond sandbox and should become the new reference | [Example] |
| Data/API constraint | Production behavior changed due to real integration constraints | [Example] |

## Review Cadence

| Review | Participants | Cadence | Output |
|---|---|---|---|
| Build drift review | XD + Engineering | [Cadence] | Update drift log and backlog |
| Release learning review | Product + XD + Engineering + QE | [Cadence] | Update context and patterns |

## Resolution Checklist

- [ ] Drift item is documented.
- [ ] Reason is clear.
- [ ] Decision is captured.
- [ ] Backlog follow-up exists if needed.
- [ ] Context files are updated if the decision changes intent.
- [ ] Sandbox is updated if it remains the active reference.
