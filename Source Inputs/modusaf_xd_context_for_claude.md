# ModusAF + Experience Design Integration Context

## How to use this document

Use this as the starting context for continuing the ModusAF Experience Design work in Claude.

The immediate task is to continue developing the Experience Design context pack templates as an extension to the Product Leadership context pack. Do not create a competing product context system. Treat Product Leadership as the product spine and Experience Design as the experience implementation context layer.

When continuing the work, optimize for practical operating artifacts: markdown templates, repo structure, backlog fields, review checklists, and handoff standards that a delivery team can actually use.

---

## Core purpose

Modus is building an agentic SDLC operating model called ModusAF.

ModusAF is intended to help cross-functional teams move faster from product intent to working software by using AI-enabled workflows, durable context, agent-ready backlog practices, and clearer quality gates across the delivery lifecycle.

Experience Design must be embedded in this framework as an operating function, not treated as a downstream artifact function.

The objective is to define how XD contributes to ModusAF through:

- product sensemaking
- experience context authoring
- coded Experience Sandboxes
- AI-ready backlog inputs
- interaction and state definition
- accessibility and usability expectations
- experience quality governance
- release learning and measurement

The working thesis is simple:

If XD creates better experience context earlier through structured markdown, coded sandboxes, and AI-ready backlog inputs, then Product, Engineering, QE, and agents can move faster with less ambiguity, lower rework, and stronger product outcomes.

---

## What ModusAF is

ModusAF is not only a toolset. It is a way of working across the SDLC that uses AI, agents, shared context, and human governance to improve speed, clarity, and delivery quality.

It aligns to the Modus delivery model:

- Align: create shared clarity on intent, constraints, and outcomes.
- Define: turn aligned intent into a buildable, testable delivery plan.
- Build: deliver working software with continuous validation and feedback.
- Evolve: sustain, measure, and expand value in real-world use.

ModusAF is supported by persistent AI foundations, including:

- LLM intelligence
- context and memory
- MCP
- agent orchestration
- feedback automation
- governance and human-in-the-loop oversight

The goal is not blind automation. The goal is to make human and AI-assisted delivery more effective by giving teams clearer context, better decision traceability, stronger implementation inputs, and more explicit quality standards.

---

## Why XD belongs in ModusAF

Agentic delivery is only as good as the context it receives.

AI agents can accelerate synthesis, backlog generation, code scaffolding, testing, refactoring, implementation, and feedback analysis. But agents cannot reliably infer product intent, user behavior, workflow logic, accessibility needs, interaction states, content meaning, or experience quality from vague tickets or disconnected artifacts.

Experience Design closes that gap.

XD defines the human, behavioral, structural, and experiential context that allows teams and agents to build the right product with less ambiguity.

XD helps ModusAF answer:

- Who is this product for?
- What job or workflow are users trying to complete?
- What behavior change matters?
- What paths, states, roles, and edge cases must be supported?
- How should the product be organized?
- What content and terminology should remain consistent?
- What components and patterns should guide implementation?
- What accessibility and usability expectations must be met?
- What does experience quality mean before demo, launch, or handoff?
- How will we know the experience is working in real use?

The operating principle:

Move as fast as the product context allows, but no faster than the experience can remain coherent, usable, accessible, and fit for purpose.

---

## Relationship to Product Leadership

The Product Leadership team has already created a product context pack. That pack should be treated as the shared product spine.

The XD context pack should not duplicate it.

Product Leadership owns the product intent and decision spine:

- business goals
- business outcomes
- value hypotheses
- prioritization rationale
- scope tradeoffs
- success measures
- adoption scorecards
- release learning
- decision cadence
- backlog readiness
- stakeholder alignment

XD extends that spine with the experience implementation layer:

- design operating mode
- experience intent
- users, tasks, and roles
- journeys and flows
- information architecture and object model
- sandbox manifest
- interaction states
- components and patterns
- content and language
- accessibility and usability expectations
- experience acceptance
- experience measurement

The clean model:

- Product Leadership defines why we are building, what value matters, what bets we are making, and how adoption will be measured.
- Experience Design defines what the product experience must be, how it behaves, how the sandbox expresses it, what engineers and agents need to preserve, and how experience quality will be accepted.
- Engineering defines how the production system is architected, implemented, tested, and maintained.
- QE defines how release quality is validated, evidenced, and protected.

Do not create separate XD versions of PL-owned files such as business intent, value flow, adoption scorecard, release learning map, or decision log. Instead, add XD-specific fields, tags, prompts, and references where needed.

---

## Product Leadership context pack integration guidance

The PL pack should remain the source of truth for:

- business intent
- value flow
- requirement hierarchy
- decision log
- release learning
- adoption scorecard
- backlog export readiness
- general prompt library
- product-level AI readiness

The XD pack should sit beside it as an extension layer.

Recommended structure:

```text
/context
  /product-context
    00_README.md
    00_source_inputs/
    01_business_intent.md
    02_value_flow_map.md
    03_requirement_hierarchy.md
    04_decision_log.md
    05_living_specs/
    06_release_learning_map.md
    07_adoption_scorecard.md
    08_ai_review_notes.md
    09_backlog_export_ready.md
    10_prompt_library.md
    11_templates_and_standards/

  /experience-context
    00_experience_mode.md
    01_experience_intent.md
    02_users_tasks_roles.md
    03_journeys_flows.md
    04_ia_object_model.md
    05_sandbox_manifest.md
    06_interaction_states.md
    07_components_patterns.md
    08_content_language.md
    09_accessibility_usability.md
    10_experience_acceptance.md
    11_experience_measurement.md
    12_research_validation.md
    13_ai_experience_patterns.md

  /agent-instructions
    AGENTS.md
    prompt_library.md
    review_checklists.md

/experience-sandbox
  README.md
  routes.md
  mock_data.md
  handoff_notes.md
  drift_log.md
```

---

## MVP focus

The MVP is focused on Mode 1: Code-First Product Shaping.

This mode applies to greenfield, utility-oriented products where working software creates more value than static design fidelity.

Best-fit product types:

- internal tools
- operator-facing B2B applications
- workflow automation products
- dashboards
- admin tools
- quote intelligence tools
- document review tools
- exception handling workflows
- back-office utilities
- AI-assisted task environments

These products usually have:

- narrow or well-understood users
- low-to-moderate brand requirements
- limited need for bespoke visual design
- high need for clarity, speed, and task completion
- no mature client design system to preserve
- strong value in seeing and testing working flows early

This is the right first target because it gives Modus the most upside with the least governance risk.

---

## MVP non-goals

Do not dilute the first version by trying to solve every design-to-code workflow.

The MVP should not include:

- designers directly editing production code as a standard expectation
- designer-owned production pull requests
- mature client design-system governed delivery
- complex bidirectional Figma-to-code and code-to-Figma workflows
- heavily branded B2C experiences
- regulated or high-risk product environments
- brownfield products with complex existing component ecosystems
- client design systems with strict approval requirements
- broad replacement of existing product, engineering, or QE processes
- proving that sandbox code can be reused one-to-one in production

These are future-state questions. They should not slow down the MVP.

---

## Design operating modes

Every project should declare a design operating mode before delivery begins. The selected mode determines how XD works, how much Figma is needed, whether a sandbox is appropriate, what context files are required, and what experience quality gates apply.

The team should always choose the lightest responsible design workflow.

### Mode 0: Opportunity and Product Definition

Use when the team does not yet know exactly what to build.

XD leads discovery, workflow understanding, product framing, concept development, and validation planning.

Primary outputs:

- opportunity brief
- product intent contribution
- audience and user hypotheses
- current-state journey or workflow
- future-state concept options
- riskiest assumptions
- validation plan
- target experience narrative
- decision log contribution

Exit criteria:

The team has a clear product direction, defined users, prioritized assumptions, and enough confidence to move into Mode 1, 2, or 3.

### Mode 1: Code-First Product Shaping

Use for greenfield utility and workflow products. This is the MVP focus.

XD defines the product shape, user flows, IA, interaction behavior, content expectations, accessibility expectations, UX acceptance criteria, and coded Experience Sandbox.

Figma is optional. Use Figma only when it reduces ambiguity.

Primary artifact:

Experience Sandbox: a coded mock/prototype app that demonstrates the intended experience using mock/demo data and approved UI foundations.

### Mode 2: Brand-Aware Accelerated MVP

Use when speed matters, but brand, credibility, trust, or customer-facing quality also matter.

XD may use both a sandbox and selective Figma artifacts for brand-critical or high-ambiguity moments.

Non-negotiable:

The MVP must not feel generic by accident. Any simplification of brand or design-system fidelity must be intentional and documented.

### Mode 3: Design-System Governed Delivery

Use when the product must fit into a mature product, brand, design system, regulated environment, brownfield ecosystem, or strict approval process.

Figma and design-system governance are required.

Non-negotiable:

Do not use agentic acceleration as an excuse to bypass system governance.

---

## The Experience Sandbox

The Experience Sandbox is the primary new XD artifact in the MVP.

It is a coded mock/prototype environment created by XD using an AI-enabled IDE such as Claude Code, Cursor, or a similar tool.

It is not the production app.

It is a working experience model that demonstrates product flows, routes, interaction behavior, states, representative data, content, and usability intent before engineering implementation.

The sandbox should help Product, Engineering, QE, stakeholders, and AI agents understand what should be built and what good looks like.

The value of the sandbox is not primarily code reuse. The value is experience clarity.

### The sandbox should show

- primary user flows
- core screens and routes
- navigation model
- task progression
- representative mock data
- empty states
- loading states
- error states
- success states
- form behavior
- validation behavior
- permissions or role differences where relevant
- important interaction patterns
- content and terminology
- responsive expectations where relevant
- accessibility intent where feasible

### The sandbox should use

- approved component libraries where possible
- agreed UI conventions
- mock or demo data
- clear file naming
- clear route naming
- simple state models
- lightweight documentation
- supporting context files

### The sandbox should not be treated as

- production-ready code
- a replacement for engineering planning
- a substitute for architecture
- a complete application
- a bypass around code review
- a place for unmanaged design experimentation after implementation begins
- a source of truth that drifts without governance

The sandbox is implementation context, not the implementation itself.

---

## Production code boundary

For MVP, code-first does not mean designers edit production code.

The correct boundary:

- XD owns experience intent and coded experience exploration.
- Engineering owns production implementation, architecture, code quality, integration, production pull requests, and merge readiness.

Designers may create coded sandboxes. Engineers may reuse sandbox code where useful, but they are not obligated to. Production quality remains an engineering responsibility.

This is safer and more useful than asking designers to become production front-end engineers as the default expectation.

---

## Recommended repository model

For the MVP, the Experience Sandbox should remain separate from production implementation.

Start with one of these models:

### Option A: Separate repo

Best when:

- the product is early-stage
- implementation has not started
- design needs freedom to iterate
- production architecture is not stable
- the team wants clean separation of responsibility

Tradeoff:

- engineering must pull context from a separate repo
- drift between sandbox and implementation must be managed

### Option B: Subrepo or dependency

Best when:

- the team wants closer alignment
- engineering wants easier access to sandbox context
- sandbox may become reusable implementation input
- the team has enough Git maturity to manage dependencies

Tradeoff:

- more setup complexity
- governance must be clearer

### Option C: Same repo, separate sandbox area

Best when:

- the team is small
- engineering wants tight visibility
- the app architecture supports separation
- designers are comfortable working in the repo

Tradeoff:

- higher risk of confusion between sandbox and production code
- requires stronger branch, review, and permission practices

Recommendation for first pilot:

Start with Option A or B. Do not start with designers editing production implementation directly.

---

## AI-ready backlog standard

A backlog item is AI-ready when an engineer or agent can implement with limited interpretation.

For front-end or experience-heavy stories, a written ticket is not enough.

An AI-ready story should include:

- product intent
- user/job context
- flow context
- Experience Sandbox reference
- interaction behavior
- component guidance
- content guidance
- accessibility expectations
- acceptance criteria
- open questions
- instrumentation needs where relevant

A ticket is not AI-ready if the agent must invent the layout, interaction model, user intent, component choices, state behavior, or content meaning.

The backlog should not simply say, Build what is in the prototype. It must explain what matters, what can change, what must not drift, and what remains unresolved.

Recommended rule:

A ticket must not depend on tribal knowledge, Slack threads, or unversioned documents.

A ticket may and should reference canonical context pack files, sandbox routes, specs, and linked decisions when those sources are versioned, current, and explicitly named.

---

## AI-ready story extension

Use this as an XD extension to PL-owned feature, epic, and story templates.

```markdown
## Experience Reference

- Design operating mode:
- Sandbox route/screen/state:
- Sandbox branch or commit:
- Figma reference, if required:
- Context files:
- Related decision log entries:

## User and Flow Context

- Primary user:
- User job/task:
- Flow or journey step:
- Entry point:
- Exit condition:
- Role/permission implications:

## Interaction Behavior

- Default state:
- Loading state:
- Empty state:
- Error state:
- Success state:
- Validation rules:
- Confirmation/undo/cancel behavior:
- Edge cases:

## Component and Pattern Guidance

- Approved components:
- Layout expectations:
- Data display pattern:
- Form/input pattern:
- Modal/drawer/popover use:
- Known component gaps:

## Content Guidance

- Required labels:
- Button copy:
- Helper text:
- Error copy:
- Empty-state copy:
- Terminology constraints:

## Accessibility Expectations

- Keyboard behavior:
- Focus behavior:
- Screen reader expectations:
- Contrast/readability expectations:
- Responsive behavior:

## Measurement and Instrumentation

- Measurement hypothesis:
- User behavior signal:
- Friction signal:
- Instrumentation events:
- Baseline needed:

## UX Acceptance Criteria

- [ ] Critical task can be completed end to end.
- [ ] Intended state behavior is implemented.
- [ ] Required content is present and accurate.
- [ ] Accessibility expectations are met or risk-accepted.
- [ ] Known experience debt is documented.
```

---

## Experience measurement

Every major epic or feature should begin with a measurement hypothesis.

PL owns value and adoption measurement. XD owns experience behavior measurement.

A complete measurement model should include both.

### PL-owned measurement

- business outcome
- adoption signal
- activation/usage target
- revenue, cost, risk, or efficiency signal
- leading and lagging indicators
- release learning cadence

### XD-owned measurement

- task success signal
- friction signal
- comprehension signal
- abandonment or recovery signal
- accessibility/usability risk
- content clarity signal
- experience debt signal

Recommended measurement template:

```markdown
## Measurement Hypothesis

We believe this experience change will improve:

- user behavior:
- business outcome:
- adoption signal:
- friction signal:
- quality signal:

We will know this is working when:

- leading indicator:
- lagging indicator:
- baseline needed:
- instrumentation needed:
- review cadence:
- owner:

Implementation requirements:

- events to capture:
- properties needed:
- dashboards/reports:
- release milestone:
- follow-up decision date:
```

---

## XD context pack structure

The XD context pack should live beside the PL context pack as an extension layer.

Recommended files:

```text
/experience-context
  00_experience_mode.md
  01_experience_intent.md
  02_users_tasks_roles.md
  03_journeys_flows.md
  04_ia_object_model.md
  05_sandbox_manifest.md
  06_interaction_states.md
  07_components_patterns.md
  08_content_language.md
  09_accessibility_usability.md
  10_experience_acceptance.md
  11_experience_measurement.md
  12_research_validation.md
  13_ai_experience_patterns.md
```

### 00_experience_mode.md

Defines selected mode, rationale, role of Figma, role of sandbox, required artifacts, intentionally omitted artifacts, review model, handoff model, and quality gates.

### 01_experience_intent.md

Translates product intent into user behavior, task success, experience principles, and what must not drift.

### 02_users_tasks_roles.md

Captures users, jobs, task context, role/permission implications, expertise level, environment, constraints, and accessibility considerations.

### 03_journeys_flows.md

Defines hero flows, secondary flows, edge cases, handoffs, empty/error paths, onboarding, and flow-level acceptance.

### 04_ia_object_model.md

Documents routes, navigation, object model, terminology, relationships, visibility rules, filters, search, sorting, and responsive implications.

### 05_sandbox_manifest.md

The key bridge between XD sandbox and PL backlog.

Maps sandbox routes/screens/states to user flows, product outcomes, linked epics/stories, interaction behavior, component assumptions, content notes, accessibility expectations, open questions, and implementation relevance.

### 06_interaction_states.md

Defines behavior across default, loading, empty, error, success, validation, confirmation, permissions, notifications, keyboard behavior, mobile/touch behavior, and edge cases.

### 07_components_patterns.md

Defines approved components, component library assumptions, pattern usage, layout conventions, form patterns, data display, modals/drawers/popovers, status/feedback patterns, known gaps, and design debt.

### 08_content_language.md

Defines labels, terminology, helper text, error copy, empty-state copy, tone, reading level, domain vocabulary, and prohibited language.

### 09_accessibility_usability.md

Defines accessibility target, keyboard/focus expectations, contrast, screen reader considerations, responsive behavior, browser/device support, readability, and usability validation needs.

### 10_experience_acceptance.md

Defines UX acceptance criteria, design QA checklist, usability checks, accessibility checks, launch blockers, acceptable experience debt, and signoff model.

### 11_experience_measurement.md

Connects experience hypotheses to task success, friction signals, instrumentation needs, adoption learning, and backlog measurement.

### 12_research_validation.md

Defines assumptions, research questions, validation methods, participants, test scripts, feedback capture, decision criteria, and evidence needed before build or scale.

### 13_ai_experience_patterns.md

Required when the product includes user-facing AI behavior. Defines user control, human-in-the-loop moments, confidence/uncertainty handling, generated content review, explainability, error recovery, audit trail, trust, and prohibited AI behaviors.

---

## Required vs. optional by mode

Use this as a starting standard. It can be refined as the pack matures.

| File | Mode 0 | Mode 1 | Mode 2 | Mode 3 |
|---|---|---|---|---|
| 00_experience_mode | Required | Required | Required | Required |
| 01_experience_intent | Required | Required | Required | Required |
| 02_users_tasks_roles | Required | Required | Required | Required |
| 03_journeys_flows | Required | Required | Required | Required |
| 04_ia_object_model | Light | Required | Required | Required |
| 05_sandbox_manifest | Optional | Required | Recommended | Optional |
| 06_interaction_states | Light | Required | Required | Required |
| 07_components_patterns | Optional | Required | Required | Required |
| 08_content_language | Optional | Recommended | Required | Required |
| 09_accessibility_usability | Required | Required | Required | Required |
| 10_experience_acceptance | Optional | Required | Required | Required |
| 11_experience_measurement | Recommended | Required | Required | Required |
| 12_research_validation | Required | Recommended | Recommended | Recommended |
| 13_ai_experience_patterns | If relevant | If relevant | If relevant | If relevant |

---

## Sandbox manifest expectations

The sandbox manifest is the most important new file for the MVP.

Without it, the sandbox risks becoming a cool prototype instead of structured implementation context.

The manifest should map:

```text
Sandbox route / screen / state
-> user flow
-> product outcome
-> linked epic/story
-> interaction behavior
-> component assumptions
-> content notes
-> accessibility expectations
-> open questions
-> implementation relevance
```

Recommended route entry:

```markdown
## Route: /example-route

- Flow:
- User/job:
- Product outcome:
- Linked epic/story:
- Sandbox status: draft / reviewed / approved / deprecated
- Implementation relevance: reference-only / partial reuse possible / behavior source of truth
- Required states:
  - default:
  - loading:
  - empty:
  - error:
  - success:
- Components/patterns used:
- Data/mock data used:
- Content notes:
- Accessibility expectations:
- Open questions:
- Engineering notes:
- QE notes:
- Last reviewed:
- Owner:
```

---

## Experience AI readiness gate

Modify any PL AI readiness gate that assumes Figma frames are required for every visual story.

Recommended standard:

Every experience-heavy story must link to the approved source of experience intent. The required source depends on the selected design mode.

### Mode 1

- Experience Sandbox route, screen, state, or branch
- Supporting context file
- Optional Figma frame only where ambiguity requires it

### Mode 2

- Experience Sandbox reference
- Figma frame for brand-critical or high-ambiguity screens
- Brand/content guidance where relevant

### Mode 3

- Figma node-level frame
- Design system component mapping
- Required component/state matrix
- Sandbox reference only if used as supporting implementation context

### Experience readiness checklist

A story is experience-ready when:

- selected design mode is documented
- experience reference exists and matches the selected mode
- core flow is represented
- default/loading/error/empty/success states are covered where relevant
- component guidance is explicit
- content is exact where implementation depends on it
- accessibility expectations are stated
- measurement/instrumentation expectations are stated
- open experience questions are documented

---

## MVP workflow

### Step 1: Select the operating mode

Every project starts by selecting a design operating mode.

For MVP, the target should usually be Mode 1 unless the project has meaningful brand, system, regulatory, or stakeholder approval complexity.

Output:

- selected mode
- rationale
- role of Figma
- role of Experience Sandbox
- required context files
- design review model
- engineering handoff model

### Step 2: Create the starter context pack

Before generating UI or building the sandbox, the team creates a starter context pack.

Output:

- minimum context files
- initial experience intent
- users/tasks/roles
- core flows
- IA and route assumptions
- component/library assumptions
- interaction and accessibility expectations

### Step 3: Build the Experience Sandbox

XD uses an AI-enabled IDE to create a coded mock/prototype app.

The sandbox should start from approved defaults:

- preferred front-end stack
- approved component library
- baseline accessibility expectations
- layout conventions
- file/folder conventions
- mock data conventions
- context file structure
- prompting/instruction standards

### Step 4: Review the sandbox with Product and Engineering

Review should focus on:

- Does the flow solve the intended problem?
- Are the roles, tasks, and states clear?
- Is the IA understandable?
- Are interaction behaviors explicit?
- Is the component approach feasible?
- Are there architecture or implementation concerns?
- Is there enough context for engineering or agents to act?
- What needs to be clarified before backlog refinement?

### Step 5: Convert sandbox output into AI-ready backlog

Each relevant story should reference:

- context pack files
- sandbox routes/screens/states
- relevant flows
- component guidance
- behavior rules
- acceptance criteria
- known gaps
- implementation notes

### Step 6: Engineering implementation

Engineering implements against the backlog, context pack, and sandbox reference.

Engineering may reuse sandbox code where appropriate, but is not obligated to do so.

Engineering owns:

- architecture
- production quality
- code standards
- integration
- testing approach
- merge readiness
- technical debt decisions
- production implementation

### Step 7: Experience QA

XD reviews implemented software against experience intent.

Review should cover:

- flow completion
- task clarity
- IA and navigation
- component consistency
- interaction behavior
- content clarity
- error handling
- loading and empty states
- accessibility
- responsive behavior
- brand/system fit where relevant
- acceptable design debt

### Step 8: Capture decisions and update context

After implementation, update the context pack and decision log.

Capture:

- what changed from the sandbox
- why it changed
- what became reusable
- what became design debt
- what patterns should be used again
- what prompts/context should be improved
- what needs to be reflected in future sandbox starters

---

## Role clarity

### Experience Design owns

- product sensemaking contribution
- user context
- task and workflow understanding
- IA and flow structure
- interaction intent
- content clarity
- accessibility expectations
- coded Experience Sandbox
- UX acceptance criteria
- experience QA
- decision capture from an experience standpoint

### Product Leadership owns

- product goals
- business outcomes
- prioritization
- roadmap decisions
- scope tradeoffs
- backlog readiness
- stakeholder alignment
- success measures
- release sequencing
- adoption measurement

### Engineering owns

- technical architecture
- production implementation
- code quality
- system integration
- engineering standards
- production pull requests
- implementation planning
- technical review
- merge readiness

### QE owns

- test strategy
- functional validation
- regression coverage
- release quality evidence
- defect management
- automation strategy where applicable

### Shared ownership

- AI-ready backlog
- acceptance criteria
- context pack governance
- experience quality gates
- sandbox-to-implementation workflow
- design/engineering review cadence
- reusable patterns
- release readiness
- experiment learning

---

## Quality gates

### Gate 1: Product Direction

Before sandbox work begins, the team must understand:

- who the product is for
- what workflow is being addressed
- what user outcome matters
- what business outcome matters
- what is out of scope
- what assumptions remain unresolved

### Gate 2: Experience Structure

Before major UI generation, the team must define:

- primary user journeys
- page/route structure
- major objects and data relationships
- role and permission implications
- core interaction patterns
- known edge cases

### Gate 3: Sandbox Readiness

Before the sandbox becomes implementation input, the team must confirm:

- core flows are represented
- major screens/routes are included
- key states are visible
- mock/demo data is sufficient
- component usage is realistic
- interaction behavior is clear
- engineering has reviewed feasibility
- open questions are documented

### Gate 4: AI-Ready Backlog

Before engineers or agents implement front-end stories, the backlog must include:

- product intent
- user context
- sandbox reference
- interaction behavior
- component guidance
- content guidance
- accessibility expectations
- acceptance criteria
- known constraints

### Gate 5: Experience Acceptance

Before demo, launch, or handoff, the team must confirm:

- critical flows work end to end
- design intent is preserved
- usability issues are resolved or documented
- accessibility expectations are met or risk-accepted
- known design debt is documented
- client/system constraints are satisfied
- decision log is current

---

## Success measures

Judge the MVP by practical delivery improvement, not AI novelty.

Measure:

- time to first credible experience model
- time from product intent to AI-ready backlog
- engineering comprehension of intended experience
- number of clarification cycles before implementation
- amount of UX rework after build starts
- quality of state/error/edge-case coverage
- usefulness of sandbox to engineering and agents
- experience QA findings before demo or release
- stakeholder confidence in the direction
- team confidence in repeating the workflow

The MVP is successful if it creates a clearer, faster, more actionable path from intent to implementation without increasing production code risk.

---

## First 30-day plan

### Week 1: Define the starter kit

Create the first Mode 1 starter kit:

- Experience Sandbox repo template
- minimum context pack
- AI-ready backlog template
- sandbox review checklist
- experience QA checklist
- recommended component library
- mock data conventions
- basic prompting/instruction guidance

Decisions needed:

- name and repo model for the sandbox
- required files for Mode 1 context pack
- initial component/library preference

### Week 2: Run a pilot scenario

Select one representative workflow and build a small Experience Sandbox.

Recommended pilot types:

- quote intake/review
- complaint triage
- document extraction/review
- exception handling
- operator dashboard

Goal:

Build enough of the sandbox to test whether it improves alignment and backlog readiness.

### Week 3: Convert sandbox to backlog

Translate the sandbox into AI-ready implementation stories.

Engineering reviews for:

- clarity
- feasibility
- missing context
- implementation risk
- whether agents could act on the backlog

QE reviews for:

- testability
- acceptance criteria
- validation gaps
- release evidence needs

### Week 4: Evaluate and codify

Run a short retro and update the starter kit.

Evaluate:

- Did the sandbox reduce ambiguity?
- Did engineering understand the intended experience faster?
- Did the backlog improve?
- What still required human clarification?
- Was code review burden reduced, increased, or unchanged?
- What parts of the sandbox were reusable?
- What should remain reference-only?
- What should be standardized next?

Output:

- revised starter kit
- workflow diagram
- lessons learned
- decision log
- recommendation for next pilot

---

## Non-negotiables

1. Every project must declare a design operating mode.
2. The MVP starts with Mode 1 utility and workflow products.
3. Code-first does not mean production-code-first.
4. The Experience Sandbox is implementation context, not production software.
5. Engineering owns production implementation.
6. XD owns experience intent, context, sandbox expression, and experience quality review.
7. Figma is used where it reduces risk, not where it creates theater.
8. Interaction behavior must be documented.
9. Accessibility is part of the design brief, not downstream cleanup.
10. Decisions must be captured as durable context.
11. The XD pack must extend the PL pack, not compete with it.
12. The team must optimize for outcomes, not artifacts.

---

## Current working direction

Continue building and refining the XD Context Pack Template.

The pack should become a reusable starter kit for Mode 1 projects inside ModusAF.

The next work should focus on:

- tightening each markdown template to match PL pack fidelity
- clarifying required versus optional files by mode
- strengthening the sandbox manifest and sandbox governance model
- refining the AI-ready story extension
- adding Jira/Linear field mappings
- making the templates useful for Claude Code/Cursor workflows
- ensuring every template supports both human teams and AI agents
- keeping the tone practical, direct, and delivery-ready

---

## Recommended framing

This is not a redesign of the whole SDLC.

This is a disciplined MVP experiment that proves how XD can create better implementation context for human and AI-assisted delivery.

Core thesis:

If XD creates better experience context earlier through structured markdown, coded sandboxes, and AI-ready backlog inputs, then engineering and agents can move faster with less ambiguity, lower rework, and stronger product outcomes.

Desired outcome:

Less ambiguity before build. Better context for agents. Faster engineering comprehension. Lower rework. Stronger product experience.

---

## Instructions for Claude continuing this work

When continuing this initiative, follow these rules:

1. Preserve the PL/XD ownership split. Do not duplicate the PL context pack.
2. Build XD as an extension layer focused on experience implementation context.
3. Keep Mode 1 as the MVP focus.
4. Treat the Experience Sandbox as the primary new artifact.
5. Keep production code ownership with Engineering.
6. Write templates in operational markdown, not strategy prose.
7. Include purpose, owner, inputs, required sections, completion standard, quality checklist, and prompts in each template.
8. Make every template useful to both humans and agents.
9. Avoid unnecessary design jargon.
10. Prefer concise, directive language.
11. Make all context durable, versionable, and easy to reference from Jira/Linear.
12. Include measurement and instrumentation wherever backlog work is being shaped.
13. Capture what must not drift.
14. Explicitly document open questions and decision status.
15. Assume this will be used by Product Leadership, XD, Engineering, QE, and AI agents.

Next best task:

Open the XD context pack template and continue refining each file to match the fidelity of the PL context pack, starting with:

1. `00_experience_mode.md`
2. `05_sandbox_manifest.md`
3. `06_interaction_states.md`
4. `10_experience_acceptance.md`
5. `11_experience_measurement.md`
6. `experience_ai_readiness_gate.md`
7. `experience_story_extension.md`

