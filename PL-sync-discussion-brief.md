# PL Sync — Discussion Brief

**Meeting:** First working session with Product Leadership on ModusAF context packs
**Duration:** 60 min
**Your goal:** Wire the XD layer into their spine together, and leave with a pilot picked. Working session, not a walkthrough of 27 files.

---

## The frame (open with this)

"You built the product spine. I've built the experience layer to plug into it and refined it down to something lean. Today's about deciding together how it lands in your workflow — and picking something real to try it on."

This is a build-together session with people who are expecting your adds. So the energy is collaborative: bring recommendations as *starting points* to react to, not positions to defend. Move fast through what's settled, spend the time where their input actually shapes it.

## Two things to walk out with

1. **Agreement on how the two packs connect** — the ownership split, the shared decision log, and how experience shows up in the backlog.
2. **A pilot picked** — one real Mode 1 workflow to run the whole loop on.

If the hour gets short, these are the two that matter. Everything else can go async.

## Where it stands (quick status)

- Studied both packs; built the XD extension layer and then tightened it hard — 27 files, one source of truth per concept, a first-timer on-ramp.
- Added two things that make it operational: a **Modus Experience Standards** defaults layer (house positions on accessibility, states, responsiveness, content — projects inherit and record only deltas), and an **intake workflow** that turns raw transcripts/research into drafted context + a discovery backlog.
- `PL_INTEGRATION.md` already maps each of their files to its XD contribution — put it on screen; it does a lot of the talking.

## Decisions to make together

Each has a recommendation to react to — treat them as drafts, not asks.

**1. Ownership split — confirm it.**
PL owns why/what/value/prioritization/adoption. XD owns experience implementation (flows, IA, interaction, content, accessibility, acceptance). Engineering owns production. *Recommendation: adopt as-is; spend the time only on the grey zones below.*

**2. One shared decision log, discipline-tagged.**
One log (theirs), XD contributes entries tagged `[Experience]`. It's also how learning flows back into the standards over time. *Recommendation: adopt the tags; XD writes into the same log.*

**3. How experience shows up in the backlog.**
Add a few experience fields to their feature/epic/story templates, and have experience-heavy stories reference their experience context before they're "ready." *Recommendation: try it on the pilot first, tune it together, then decide how widely it applies.*

**4. Measurement — one model, two owners.**
Their adoption/value metrics + XD's task-success/friction signals become one measurement per feature, co-authored at kickoff. *Recommendation: XD joins the measurement-hypothesis conversation at feature start.*

**5. Design mode at kickoff.**
Every initiative declares a mode (usually Mode 1 for the MVP); it sets which artifacts and gates apply, so it fits into their intake/planning. Mostly a heads-up so it's built into the front of the process.

## Grey zones to align on together

Quick agreement here avoids overlap later:

- **Measurement** — they own adoption/value/business outcomes; XD owns task success, friction, comprehension.
- **Content** — XD owns product terminology and UI copy; they own positioning/messaging.
- **Research** — XD owns experience/usability validation; they own market/business validation.

## Questions they'll likely want to talk through

Not objections — genuine things a good partner will ask. Be ready to riff:

- How much does this add to backlog refinement, realistically? (Answer: scoped to experience-heavy stories; the intake + defaults are there to make it faster, not heavier.)
- Where's the line on the sandbox — are designers writing production code? (No; it's implementation context, engineering owns production.)
- How do we keep the two packs in sync as things change? (Shared decision log + event-based maintenance triggers; the tightening we did is itself a currency strategy — less to keep in sync.)
- Who owns the house standards / defaults layer, and should PL have an equivalent?

## Shared next steps (divide it up live)

- Confirm the decision-log tags and who wires them into the current log.
- Agree the experience fields to trial on the pilot's stories.
- Name a PL partner for the pilot.
- Pick the initiative to pilot on.

## The pilot (the concrete outcome)

Co-select one Mode 1 workflow — quote intake, complaint triage, doc review, exception handling, or an operator dashboard. Run the full loop: intent → sandbox → AI-ready backlog → build → experience QA. Then schedule the **intake dry-run** on one real transcript from it.

## Suggested run of the hour

| Time | Segment |
|---|---|
| 0–5 | Frame; "your spine + this layer, let's wire it together" |
| 5–15 | Where it stands + the extension model (PL_INTEGRATION on screen) |
| 15–35 | The five decisions — react and refine together |
| 35–50 | Pick the pilot + divide up next steps |
| 50–60 | Open questions, schedule the dry-run |

## Bonus, if there's appetite

Offer to help tidy the PL pack too — in refining the XD side you spotted similar duplication worth cleaning (hierarchy defined twice, export logic twice, ~1,500 lines of generic analysis templates). Frame it as "I can do the same pass for yours if useful."
