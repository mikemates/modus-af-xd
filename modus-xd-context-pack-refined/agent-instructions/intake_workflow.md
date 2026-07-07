# Intake Workflow: Raw Sources → Drafted Context Pack

How to turn bulk raw material — meeting transcripts, research decks, client artifacts, existing docs — into a minimally useful, structured XD context pack without laundering speculation into "context."

## Principles (read first)

- **Extract, then curate.** AI proposes drafts; a human verifies, corrects, and decides what stays open. The AI's job is not to sound finished.
- **Flag, don't fill.** Anything not grounded in a source becomes `[Open question]` or `[Assumption]`, never a confident guess.
- **Cite everything.** Each extracted claim names its source. Unattributed = not context.
- **Intent-first.** Draft `01_experience_intent`, `02_users_tasks_roles`, `03_journeys_flows` first — everything downstream references them. IA, states, and components are better *shown by the sandbox* than mined from a transcript.
- **Apply house defaults.** Where a source is silent on accessibility, states, responsiveness, or content conventions, apply Modus Experience Standards rather than inventing — and note that you did.
- **Minimally useful beats complete.** A pack 60% filled with clear open-questions is more useful than one 100% filled with guesses. Aim for the Mode 1 minimum set (see README).

---

## Step 1 — Stage and inventory the sources

Don't extract yet. Catalog what you have so claims can be attributed and weighed.

```text
You are helping build an XD context pack. Below are raw source materials.

For each source, produce one row of a source inventory:
| Source ID | What it is | Date | Author/role | Reliability (primary evidence / stated opinion / secondhand / unknown) | Topics it likely informs |

Do not summarize content yet. Only inventory. Flag anything that looks like
opinion-stated-as-fact or client politics so it isn't treated as evidence later.

SOURCES:
[paste transcripts / paste or attach docs]
```

## Step 2 — Map sources to context files

Most of a transcript is noise for XD. Route the signal.

```text
Using the source inventory and the XD context pack file list (see README
"Document Purposes"), map which sources speak to which context file.

Output a table: | Context file | Relevant Source IDs | Coverage (strong / partial / none) | Notes |

Call out files with NO source coverage — those become discovery gaps, not
invented content.
```

## Step 3 — Extract the intent-first trio

Run this once per file for `01_experience_intent`, `02_users_tasks_roles`, `03_journeys_flows`. It fills the template, flags gaps, and cites sources.

```text
Draft the [FILE NAME] context file from the mapped sources only.

Rules:
- Fill the template's sections. Use ONLY what the cited sources support.
- After each claim, add a source tag: (Src: S3, S7).
- For anything the sources don't establish, insert [Open question: ...] or
  [Assumption: ...] instead of guessing.
- Where the sources are silent on a house-default topic (accessibility, states,
  responsiveness, content conventions), write "Follows Modus Experience
  Standards" and move on — do not restate the defaults.
- Do not resolve contradictions between sources silently. Surface them as
  [Open question] with both positions.
- End with a "Confidence & gaps" note: what is well-grounded, what is thin,
  what a human must decide.

TEMPLATE:
[paste the target file's template]

SOURCES:
[paste the mapped sources for this file]
```

## Step 4 — Draft or derive the rest

Reuse the Step 3 prompt for any remaining required file. For IA (`04`), interaction states (`06`), and components (`07`), prefer to **derive from the sandbox once it exists** rather than over-extract from documents — note them as "to be confirmed via sandbox."

## Step 5 — Work it through with a human (interaction prompts)

This is where judgment lives. The person's job shifts from writing to *deciding* — and the AI's job is to interrogate the material with them and hand them concrete follow-up work, not to hand back a finished-looking document. Run these as a **loop**: the AI proposes, the human answers, the AI revises. Stop when the build-blocking questions are answered or consciously risk-accepted — not when everything is perfect.

Use them in roughly this order. 5.1 is best run *before* the Step 3 extraction; the rest after a draft exists.

### 5.1 Clarify before drafting

```text
Before you draft anything, read the mapped sources and ask ME the questions
that would most improve the result.

- List the top 7 questions, ranked by how much each would reduce ambiguity or rework.
- For each: say why it matters and which context file it affects.
- Prefer questions only a human insider can answer (tacit process knowledge,
  politics, real priorities) over things the sources already cover.

I will answer what I can and mark the rest unknown. Then draft.
```

### 5.2 Triage claims: signal vs. noise

```text
From the drafted file, list every claim you are NOT confident is a real
requirement. For each, show the claim, its source, and your read:

| Claim | Source | Your read: fact / opinion / contested / single-source / aspiration | Why |

I will label each: CONFIRM (it's a requirement) / ASSUMPTION (test it) /
OPINION (not a requirement) / DROP. Update the draft from my labels — do not
promote opinion or aspiration to requirement on your own.
```

### 5.3 Resolve contradictions

```text
List every place the sources disagree or where a source contradicts the
current draft.

| Topic | Position A (source) | Position B (source) | Why it matters |

For each, ask me to: RESOLVE (I'll pick, you record the reason as an
[Experience] decision), DEFER (I'll name an owner and due date), or
ESCALATE (needs a stakeholder). Never silently pick one.
```

### 5.4 Rank assumptions by risk

```text
Take every [Assumption] in the draft and rank it by impact-if-wrong ×
uncertainty.

| Assumption | Impact if wrong (H/M/L) | Confidence (H/M/L) | Risk tier |

Sort into: VALIDATE BEFORE BUILD / VALIDATE DURING BUILD / MONITOR.
This is my prioritized validation list — the few things worth slowing down for.
```

### 5.5 Devil's-advocate completeness check

```text
Play three skeptics in turn — a senior engineer, a product lead, and a QE
lead. For each, list what they would say is missing or too vague before they
could build, prioritize, or test from this file.

Group findings by context file. Flag anything that looks like an
unknown-unknown we haven't captured as an open question yet.
```

### 5.6 Turn gaps into discovery tasks

This is the step that arms the human with follow-up work. Every open question and risky assumption becomes an actionable inquiry.

```text
Convert every [Open question] and every "validate before/during build"
assumption into a discovery backlog. One row each:

| ID | What we need to learn | Why it matters / what it unblocks | Best method | Who / where | Priority | Target |

Pick the method using the cheat sheet below. Group by priority. Keep it to
real, assignable tasks — not "do more research."
```

### Discovery method cheat sheet

Match the *kind* of gap to the right follow-up so a non-researcher picks well:

| If the gap is about… | Best discovery method |
|---|---|
| Who the user really is, their goals, real priorities | Stakeholder / user interview |
| How often something happens, volumes, drop-off | Analytics pull or a data request |
| The rules, edge cases, or domain logic | SME session or document request |
| Whether users will understand or complete it | Usability test on the sandbox |
| Current-state workflow and workarounds | Contextual inquiry / job shadowing |
| Competing or contradictory stakeholder views | Alignment workshop / decision meeting |
| Whether the concept is desirable at all | Concept test or prototype feedback |

### Exit bar — is this "ready enough"?

- [ ] Every claim is source-cited or marked as assumption/open question.
- [ ] No source's *opinion* has been promoted to *requirement*.
- [ ] Contradictions are resolved, deferred with an owner, or escalated.
- [ ] Risky assumptions have a discovery task; build-blockers are answered or risk-accepted.
- [ ] House-default topics say "Follows Modus Experience Standards" plus deltas — not restated defaults.
- [ ] Real deviations from the defaults are logged as `[Experience]` decisions.
- [ ] The discovery backlog exists and its top items have owners.
- [ ] The file meets its own "Quality Standard" footer, or its gaps are explicit.

## Step 6 — Let the sandbox find the rest

Build the Mode 1 sandbox from the drafted trio. It is the forcing function: it can't be built where the context is genuinely missing, so it surfaces the real gaps a document review misses. Feed those gaps back as `[Open question]`s and update the files.

---

## The same pipeline keeps the pack current

This workflow is not just for day one. Run Steps 1–3 on *new* inputs (fresh transcripts, decisions, PRs) on a loop to propose updates to existing files for human approval. Initial fill and ongoing currency are the same machinery — see the pack's Maintenance triggers in the README.

## Related

- File purposes and Mode 1 minimum set: `../README.md`
- Reusable review/generation prompts: `prompt_library.md`
- House defaults referenced above: Modus Experience Standards (external, Modus-wide)
