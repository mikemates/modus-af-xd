# Getting Started

For someone opening this pack for the first time. It walks through *how* to navigate and populate the folder in order. For reference material — the full file list, purposes, and the required-files-by-mode table — see `README.md`; this guide points there instead of repeating it.

## The mental model

This pack is a set of fill-in-the-blank markdown files that describe **one product or initiative** so people and AI agents can build it without guessing. You don't fill in all of them — one early decision (your "mode") determines which files you need. The flow is: **decide how you'll work → describe the experience → build or point to a working sandbox → turn that into tickets → check quality → keep it current.**

## Step 0: Make your own copy

Don't edit the template folder. Copy it into your project or product repo and work in the copy. Every file has `[bracketed placeholders]` — those are the blanks you replace. Every file ends with a **"Quality Standard"** line telling you what "done enough" looks like; that's your finish line for that file.

## Step 1: Pick your mode

This is the decision that drives everything else. Use `templates-and-standards/mode_selection_worksheet.md` — it asks a few questions (how well you know the users, how much brand matters, how mature the design system is) and points you to a mode. Record the choice and *why* in `experience-context/00_experience_mode.md`.

Most Modus MVP work is **Mode 1 (code-first)**: greenfield internal tools, dashboards, operator apps. If that's you, the README's "Mode 1 Minimum Context Pack" lists the ~9 files to fill — ignore the rest until you need them.

## Step 2: Fill the core context files, in order

Follow the Navigation Map in the README, top to bottom. The README's "Document Purposes" explains every file; a few are worth extra attention because they carry the most weight or trip people up:

- **`01_experience_intent.md`** is your north star — what should get easier/faster/clearer, and what must *not* drift while it's built.
- **`06_interaction_states.md`** is the file agents lean on most: how things *behave* (loading, empty, error, success, validation, recovery), not just how they look.
- **`09_accessibility_usability.md`** is the single source for accessibility — fill it once and well; other files point here.
- **`11_experience_measurement.md`** is the single source for how you'll know it worked (events and signals).

**How much to write:** enough that someone who's never seen the product could build the right thing. Where you don't know something yet, don't leave a blank — mark it `[Open question]`, `[Assumption]`, or `[Needs validation]`. A blank looks finished; a marker tells everyone it isn't.

## Step 3: Build or link the Experience Sandbox

In Mode 1 the sandbox (a coded mock in Claude Code/Cursor) is your primary artifact — it *shows* the experience instead of describing it. Two files govern it:

- **`experience-context/05_sandbox_manifest.md`** — the bridge. Map each sandbox route/screen/state → flow → backlog item → what's reusable vs. reference-only. This is the most important new file; without it the sandbox is just a demo.
- **`experience-sandbox/README.md`** — travels with the sandbox code: setup, code hygiene, and how engineers/agents should use it.

## Step 4: Turn it into AI-ready tickets

For each piece of work, copy `templates-and-standards/experience_story_extension.md` into your Jira/Linear story and fill it in. Then run it through `templates-and-standards/experience_ai_readiness_gate.md` — the checklist that confirms a ticket has enough context to build without guesswork. `templates-and-standards/jira_linear_field_mapping.md` tells you which fields to add in your tool.

Rule of thumb: a ticket is ready when an engineer or agent could build it *without* asking a clarifying question or hunting through Slack.

## Step 5: Check quality at the gates

`templates-and-standards/experience_quality_review.md` is one tool used at two moments: **Sandbox Review** (before it becomes backlog) and **Experience QA** (before demo/release). Both check the same quality dimensions. Record the durable outcome — launch blockers, accepted debt, signoff — back in `experience-context/10_experience_acceptance.md`.

## Step 6: Keep it current

Log differences between the sandbox and the built product in `experience-sandbox/drift_log.md`. Capture decisions in the **shared decision log** (that lives in the Product Leadership pack — you tag entries `[Experience]`; see `PL_INTEGRATION.md`). The README's "Maintenance" table says who updates what and when.

## The four things first-timers get wrong

1. **Filling in every file.** Let the mode decide. Mode 1 needs ~9 files, not 25.
2. **Leaving blanks instead of marking unknowns.** Use `[Open question]` / `[Assumption]` / `[Needs validation]`.
3. **Treating the sandbox as the spec.** The sandbox *shows*; the manifest and tickets say what matters, what can change, and what must not drift.
4. **Restating things across files.** Accessibility lives in `09`, event naming in `11`, mode definitions in `00`. Everywhere else, reference them.

## Shortest version

README → pick mode → fill the Mode 1 files → build the sandbox → write tickets from the story template → run the gate.
