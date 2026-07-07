# Experience Quality Review

One review tool, run at two gates:

- **Sandbox Review** — before the sandbox becomes backlog input. Outcome: Approved / Approved with changes / Not ready.
- **Experience QA** — before demo, release, or handoff. Outcome: Pass / Pass with debt / Fail.

Both gates check the same experience quality dimensions at different fidelities: the sandbox review asks *"is it represented or documented?"*, QA asks *"does the built software behave?"*. Define the dimensions once (below), then run the gate you need.

For the pre-implementation ticket gate, use `experience_ai_readiness_gate.md`. For the launch go/no-go decision and debt register, use `experience-context/10_experience_acceptance.md`.

---

## Experience Quality Dimensions

| Dimension | What "good" means |
|---|---|
| Flow completion | The primary role can complete the critical task end to end. |
| IA & navigation | Labels match approved terminology; users know where they are and what to do next; role/permission visibility is correct. |
| Interaction states & behavior | Default, loading, empty, error, success, validation, and recovery (undo/cancel/retry) behave as intended. |
| Components & visual coherence | Approved components/patterns are used; variants and layout are correct; deviations are documented. |
| Content & language | Labels, button copy, error/empty/success messages are clear, actionable, and match `08_content_language.md`; placeholders are removed or accepted as debt. |
| Accessibility & usability | Keyboard paths work, focus order is logical and managed, screen-reader semantics are acceptable, status is not color-only, required breakpoints work. |
| Measurement & instrumentation | Required events exist with correct triggers and properties; friction signals are observable. |

The AI readiness gate uses these same dimensions to decide whether a *ticket* carries enough context. Keep the three in sync — this table is the shared source.

---

## Gate A — Sandbox Review (before backlog)

Run when Product, XD, Engineering, and QE review the Experience Sandbox before it becomes backlog input.

**Project:** [Name]  ·  **Sandbox version:** [Branch/tag/commit]  ·  **Date:** [YYYY-MM-DD]  ·  **Participants:** [Names]

### Product & experience fit

- [ ] Sandbox reflects current product intent.
- [ ] Primary role and task are clear; core flow solves the intended problem.
- [ ] Flow has a clear entry and completion point.
- [ ] Non-goals and missing areas are explicit.

### Dimension checks (represented or documented)

- [ ] **Flow completion** — major routes/screens represented; critical flow is walkable.
- [ ] **IA & navigation** — navigation model understandable; object/list/detail relationships and role/permission implications visible or documented.
- [ ] **Interaction states** — default, loading, empty, error, success represented or documented; validation and recovery understandable.
- [ ] **Components** — usage realistic; library assumptions documented; custom components flagged; reusable vs. reference-only identified.
- [ ] **Content** — key labels/messages clear; placeholders marked; terminology matches context files.
- [ ] **Accessibility** — keyboard/focus expectations documented; risks visible.
- [ ] **Measurement** — instrumentation implications visible.

### Backlog readiness

- [ ] Routes/states map to features, epics, or stories.
- [ ] Acceptance criteria and measurement implications are clear.
- [ ] Open questions are documented.
- [ ] Sandbox manifest (`05_sandbox_manifest.md`) is updated.

### Findings & decision

| Finding | Severity | Decision / action | Owner |
|---|---|---|---|
| [Finding] | Low / Med / High / Blocker | [Action] | [Owner] |

**Decision:** Approved / Approved with changes / Not ready
**Required changes before backlog:** [List]
**Decision log link:** [Link]

---

## Gate B — Experience QA (before demo / release)

Run during sprint reviews, demos, release readiness, and pre-handoff QA against built software.

**Project:** [Name]  ·  **Build / environment:** [URL]  ·  **Date:** [YYYY-MM-DD]  ·  **Reviewer(s):** [Names]  ·  **Related sandbox version:** [Branch/tag/commit]

### Dimension checks (built software behaves)

- [ ] **Flow completion** — critical flows work end to end for the primary role.
- [ ] **IA & navigation** — labels/routes match approved IA or documented decisions; location and next action are clear; role/permission visibility behaves.
- [ ] **Interaction states** — default, loading, empty, error, success/confirmation behave; validation triggers appropriately; undo/cancel/retry works where required.
- [ ] **Components** — approved components and correct variants/states used; layout consistent; deviations documented.
- [ ] **Content** — labels, action language, error/empty/success copy correct; placeholders removed or accepted as debt.
- [ ] **Accessibility** — required keyboard paths, focus order and management, screen-reader semantics, non-color status, and breakpoints all work.
- [ ] **Measurement** — required events implemented with correct triggers/properties; friction signals observable.

### Findings, blockers & decision

| Finding ID | Dimension | Severity | Finding | Recommendation | Status |
|---|---|---|---|---|---|
| XDQA-001 | [Dimension] | Low / Med / High / Blocker | [Finding] | [Recommendation] | Open / Closed / Accepted |

**Launch blockers** (materially prevent task completion, break a critical flow, violate required accessibility, or undermine trust):

| Blocker | Required fix | Owner | Status |
|---|---|---|---|
| [Blocker] | [Fix] | [Owner] | Open / Fixed |

**Accepted debt** (named, understood, with a follow-up path):

| Debt item | Risk | Accepted by | Follow-up |
|---|---|---|---|
| [Debt] | [Risk] | [Name] | [Story/link] |

**Decision:** Pass / Pass with debt / Fail
**Rationale:** [Reason]
**Required follow-up:** [List]

---

## Quality Standard

This file is ready when a team can run either gate and reach a confident, evidence-based decision without relying on subjective opinion — using one shared definition of what experience quality means.

## Related Documents

- Ticket gate before implementation: `experience_ai_readiness_gate.md`
- Launch go/no-go and debt register: `../experience-context/10_experience_acceptance.md`
- Sandbox mapping: `../experience-context/05_sandbox_manifest.md`
