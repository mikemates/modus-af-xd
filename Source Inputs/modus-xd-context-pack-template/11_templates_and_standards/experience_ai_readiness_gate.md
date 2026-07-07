# Experience AI Readiness Gate

Use this gate before experience-heavy stories enter sprint planning, implementation, or agentic execution.

A backlog item is AI-ready when an engineer or agent can implement with limited interpretation using the ticket, linked Product Context Pack files, linked XD context files, and approved Experience Sandbox references.

## Core Rule

A ticket must not depend on tribal knowledge, Slack threads, meetings, or unversioned artifacts.

A ticket may reference canonical context files, sandbox routes, specs, and linked decisions when those sources are versioned, current, and explicitly named.

## Experience Reference Standard

Every experience-heavy story must link to the approved source of experience intent.

| Mode | Required experience reference |
|---|---|
| Mode 1 | Experience Sandbox route, screen, state, or branch; supporting context file; Figma only where ambiguity requires it. |
| Mode 2 | Experience Sandbox reference; Figma frame for brand-critical or high-ambiguity screens; brand/content guidance where relevant. |
| Mode 3 | Figma node-level frame; design system component mapping; required component/state matrix; sandbox only if used as supporting context. |

## Feature Readiness Criteria

| Criteria | Owner | Validation |
|---|---|---|
| Experience mode is declared | XD | `00_experience_mode.md` is current |
| Experience hypothesis is defined | Product + XD | Feature links to behavior and business outcome |
| Primary users and tasks are specific | XD + Product | `02_users_tasks_roles.md` is current |
| Primary flow is identified | XD | `03_journeys_flows.md` links to feature |
| Experience measurement is defined | Product + XD + Data | `11_experience_measurement.md` includes signals |
| Experience risks are visible | XD + Product | Risks and assumptions are documented |

## Epic Readiness Criteria

| Criteria | Owner | Validation |
|---|---|---|
| Walking skeleton is identifiable | Product + XD | End-to-end user path is documented |
| Sandbox reference exists if applicable | XD | `05_sandbox_manifest.md` maps route/state to epic |
| Key states are represented or documented | XD | State coverage matrix is current |
| Role/permission implications are clear | XD + Engineering | Users/tasks/roles and IA files are current |
| Component approach is feasible | XD + Engineering | Component file and review notes are current |
| Testability is clear | QE | QE can derive tests from acceptance criteria |

## Story Readiness Criteria

A story is experience AI-ready when all required checks pass.

### 1. Product and User Intent

- [ ] Story links to parent feature/epic.
- [ ] Story includes a specific role, not a generic user.
- [ ] Story describes a real user or business outcome.
- [ ] Story references relevant Product Context Pack item(s).

### 2. Experience Reference

- [ ] Story links to the approved experience reference for its mode.
- [ ] Mode 1 stories link to sandbox route/state/branch where applicable.
- [ ] Mode 2 stories link to sandbox and Figma/brand guidance where needed.
- [ ] Mode 3 stories link to Figma node-level frames and design system mapping.
- [ ] The reference is current and not superseded.

### 3. Flow and IA Context

- [ ] Related flow ID is named.
- [ ] Route/page is named.
- [ ] Entry and exit conditions are clear.
- [ ] Object(s) and data relationships are defined.
- [ ] Role/permission visibility rules are defined.

### 4. Interaction Behavior

- [ ] Default state is defined.
- [ ] Loading behavior is defined or not applicable.
- [ ] Empty state is defined or not applicable.
- [ ] Error state is defined or not applicable.
- [ ] Success/confirmation behavior is defined or not applicable.
- [ ] Validation behavior is defined or not applicable.
- [ ] Recovery, undo, cancel, or retry behavior is defined where relevant.

### 5. Component and Pattern Guidance

- [ ] Approved component(s) are named.
- [ ] Component variants/states are defined.
- [ ] Layout pattern is clear.
- [ ] Custom component needs are documented.
- [ ] Known component gaps are documented.

### 6. Content and Language

- [ ] Required labels are exact or marked draft.
- [ ] Error, empty, and success messages are exact where implementation depends on them.
- [ ] Terminology matches `08_content_language.md`.
- [ ] AI-generated content rules are included if relevant.

### 7. Accessibility and Usability

- [ ] Keyboard expectations are defined where relevant.
- [ ] Focus behavior is defined where relevant.
- [ ] Screen reader expectations are defined where relevant.
- [ ] Contrast/status does not rely on color alone.
- [ ] Responsive expectations are defined where relevant.

### 8. Measurement and Instrumentation

- [ ] Story includes measurement hypothesis if behavior change is expected.
- [ ] Required event(s) are named.
- [ ] Event triggers are clear.
- [ ] Event properties are listed where needed.
- [ ] Success and friction signals are linked.

### 9. Acceptance Criteria

Each AC must be observable and testable.

Required format:

```text
Given [complete starting state and role]
When [specific user action or system event]
Then [observable result]
And [exact copy, state, timing, accessibility, or instrumentation expectation if relevant]
```

ACs fail readiness when they say:

- "works as expected"
- "looks like the design"
- "handles errors"
- "shows a message"
- "loads quickly"
- "supports accessibility"

without defining observable behavior.

## Gate Outcome

| Outcome | Meaning | Action |
|---|---|---|
| Ready | Story can enter implementation | Proceed |
| Ready with known risk | Story can proceed with documented risk | Proceed with explicit owner |
| Not ready | Missing experience context creates implementation risk | Resolve gaps before implementation |
| Blocked | Critical decision, reference, or dependency missing | Escalate |

## Role Responsibilities

| Role | Responsibility |
|---|---|
| Product Leadership | Product intent, scope, prioritization, business/adoption measures |
| Experience Design | Experience reference, flows, IA, interaction behavior, content, accessibility, UX acceptance |
| Engineering | Feasibility review, production implementation implications, technical constraints |
| QE | Testability, validation strategy, regression and release evidence |
| Data / Analytics | Instrumentation feasibility, event naming, measurement validation |

## Quality Standard

This gate is working when agents and engineers stop inventing layout, interaction models, copy, state behavior, component choices, and user intent.
