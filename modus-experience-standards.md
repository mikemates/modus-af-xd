# Modus Experience Standards (House Defaults)

**Version:** 0.1
**Owner:** [Modus XD Practice Lead]
**Last Updated:** [YYYY-MM-DD]
**Status:** Active

The default experience decisions Modus applies to every project unless a client, product, or discovery finding gives a reason to differ. This is the *house floor* — teams start here instead of re-deciding basics on every engagement, and agents apply these when a project file is silent.

## How to use this (inheritance and override)

This is a **separate layer above the project XD context pack.** It is defined once, Modus-wide, and evolves over time. Project packs do **not** copy it — they inherit it and record only their **deltas**.

- A project's `09_accessibility_usability`, `06_interaction_states`, `07_components_patterns`, and `08_content_language` should say, in effect: *"Follows Modus Experience Standards vX.Y, except: [the specific things this product does differently]."*
- **Every deviation is a decision-log entry** (tagged `[Experience]`) with the reason. That is not bureaucracy — it is the mechanism by which client learning flows back into the next version of these defaults.
- When a project is silent on something covered here, **this document is the answer.** Agents should apply these defaults rather than invent.

## Two kinds of defaults

Read every item below as one of two types:

- **Standard** — expected to hold on nearly every project. Deviating requires a logged reason. (e.g., WCAG 2.2 AA, keyboard operability.)
- **Starting point** — a sensible default you *expect* to tune per client and context. Changing it is normal, not an exception. (e.g., loading thresholds, tone.)

---

## Accessibility

**Baseline: WCAG 2.2 AA. [Standard]** This is the current stable standard (ISO/IEC 40500:2025); WCAG 3.0 remains a working draft and does not supersede it. Regulated or contractually-bound work may raise this to AAA on specific criteria — record that as a project delta.

- **Keyboard operability [Standard]** — every interactive element is reachable and operable by keyboard; no keyboard traps; visible focus indicator at all times.
- **Focus management [Standard]** — focus moves to opened dialogs/drawers and returns to the trigger on close; after a destructive or async action, focus lands on the result or the next logical control; after a validation error, focus moves to the first error.
- **Screen-reader semantics [Standard]** — use native/semantic elements first; name, role, and state are programmatically available; live regions announce async status and errors.
- **Status is never color-only [Standard]** — pair color with text, icon, or shape.
- **Contrast [Standard]** — text meets 4.5:1 (3:1 for large text); UI components and focus indicators meet 3:1.
- **Reduced motion [Standard]** — respect `prefers-reduced-motion`; motion is never required to understand state.
- **Target size [Starting point]** — interactive targets ≥ 24×24px (WCAG 2.2 minimum); prefer 44×44px on touch.

Accessibility is part of the brief, not downstream cleanup. Where a project can't meet a standard, it is *risk-accepted and logged*, not silently dropped.

## Interaction states

Every interactive view handles this set by default; a project documents only where behavior differs or a state doesn't apply.

- **Default [Standard]** — the normal, populated state.
- **Loading [Starting point]** — show an indicator when a wait exceeds ~400ms; use skeletons for content areas, inline spinners for in-place actions; keep layout stable (no content jump).
- **Empty [Standard]** — never a blank screen: explain what belongs here and offer the primary next action.
- **Error [Standard]** — explain what happened, whether data was saved, and the recovery path; never a dead end; preserve user input on failure.
- **Success / confirmation [Standard]** — confirm completion; destructive or irreversible actions require explicit confirmation and, where feasible, undo.
- **Validation [Starting point]** — validate on blur and on submit (not keystroke-by-keystroke by default); messages are specific and adjacent to the field.
- **Permission / read-only [Standard]** — unavailable actions are hidden or clearly disabled with a reason; never fail silently.

## Responsiveness

- **Breakpoints [Starting point]** — design for Desktop, Tablet, Mobile. Internal/operator tools (typical Mode 1) are **desktop-first**; customer-facing work is mobile-first. State the primary context per project.
- **No horizontal scroll [Standard]** at supported widths; content reflows rather than truncates meaning.
- **Touch [Starting point]** — where touch is supported, meet the touch target size above and avoid hover-only affordances.
- **Browser/device support [Starting point]** — latest two versions of evergreen browsers (Chrome, Edge, Safari, Firefox) plus iOS Safari and Android Chrome; narrow per project.

## Content and language

- **Voice [Starting point]** — operational, direct, task-oriented; match the terms users already use in their workflow.
- **Error message structure [Standard]** — what happened → (why, if useful) → what to do next → whether data was saved.
- **Buttons [Standard]** — verb + object ("Save changes", not "OK/Submit"); destructive actions are labeled explicitly.
- **Terminology [Standard]** — one term per concept across UI, sandbox, and tickets; changes go through the glossary and decision log.
- **Reading level [Starting point]** — plain language; ~grade 8–10 for general audiences, domain terms allowed for expert operator tools.
- **AI-generated copy [Standard, when applicable]** — editable before use; uncertainty visible when confidence is low; never presented as verified unless reviewed. (See project `13_ai_experience_patterns`.)

## Components and patterns

- **Prefer accessible library components [Standard]** — use approved/accessible components before building custom; do not reinvent UI that already exists.
- **Custom components require review [Standard]** — allowed when nothing fits, but flagged for engineering + accessibility review.
- **Tokens over hard-coded values [Standard]** — color, type, spacing, radius, elevation come from the theme/token source, not magic numbers.
- **Default UI foundation [Starting point]** — [name the Modus starter component library / preferred stack here]; projects on a mature client design system override this.

## Performance (perceived)

- **Starting-point thresholds** — meaningful content within ~1s on primary views; interactive feedback within ~100ms of input; any wait over ~400ms shows a loading state. Tune per product and network context.

---

## Governance

- **Owner:** the Modus XD Practice Lead owns this document and its version.
- **How it evolves:** deviations logged across projects are reviewed periodically; recurring deviations become the next version's default. That is the whole point — the floor rises as Modus learns.
- **Versioning:** projects reference a version (`Modus Experience Standards v0.1`). Bump the minor version for additions/clarifications, major for changes that would alter existing projects' expectations.
- **Relationship to the pack:** this is the default layer; the project XD context pack is the per-product record of intent + deltas. Keep defaults here, keep specifics there — do not duplicate.

## Change Log

| Version | Date | Change | Owner |
|---|---|---|---|
| 0.1 | [YYYY-MM-DD] | Initial house defaults: accessibility, interaction states, responsiveness, content, components, performance. | [Owner] |
