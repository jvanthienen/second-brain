---
name: brain
description: Load the second-brain wiki context — the schema, the index, and the operating context. Use at the START of any chat about accounts, pipeline, meetings, customers, or updates. Triggers - brain, load my brain, catch me up, my accounts, my book, my portfolio, what do we know about, prep me for, ingest this, health-check the wiki.
---

# Brain — load the wiki

---

## Section 0 — read these first, in order

1. **`AGENTS.md`** — the schema. Page types, ingest/query/lint workflows, contradiction handling,
   honesty rules. **This governs everything you do for the rest of the conversation.**
2. **`BRAIN.md`** — who the human is, what they own, how they work.
3. **`wiki/index.md`** — the catalog. Find the relevant pages before answering.
4. **`docs/voice.md`** — before producing any written artifact.

Read them. Don't assume you remember them from a previous conversation.

---

## The three layers

| Layer | Where | Your relationship to it |
|---|---|---|
| Raw sources | `raw/` | **Read only. Never modify.** |
| The wiki | `wiki/` | **You own it entirely.** |
| The schema | `AGENTS.md` | The human owns it. Follow it. |

---

## Answering a question

1. **Read `wiki/index.md` first.** Find candidate pages.
2. Drill into them. Prefer **synthesis across pages** over quoting one.
3. **Cite page titles.**
4. If the answer sits entirely in one page, the question was probably too narrow — check whether
   a Motion or Pattern page bears on it.
5. **Offer to file good answers back as a new page.** Explorations should compound.

---

## Ingesting

Follow the Ingest workflow in `AGENTS.md` exactly. In particular:

- **8–15 pages is normal.** Two means you under-processed it.
- **Discuss takeaways before writing.** The human knows things the source doesn't carry.
- **Flag contradictions, never overwrite.** Highest-value step.
- Update `wiki/index.md` and append to `wiki/log.md`.
- Move the source out of `_inbox/`.

---

## Honesty rules

- **Never invent a number.** Didn't pull it → write `—` and say where it'd come from.
- **Never write `$0` as a placeholder.** A zero claims no revenue; a dash admits you don't know.
- **Every claim carries a source and a date.**
- **Distinguish fact from inference.** Label inferences.
- **Say what you couldn't find.**
- **"I don't know" is a complete answer.** Follow it with how you'd find out.

---

## Behaviour

- **Be resourceful before asking.** Read the index, read the page, use the tools.
- **Default to the short version.**
- **Nothing auto-sends.** Draft → human reviews → it goes.
- **Flag accounts with no activity in 14+ days.**

---

## Common requests

| Human says | Do |
|---|---|
| "Catch me up on [account]" | Read the Account page + linked Motions/Patterns/Blockers. Lead with "the one thing that matters." |
| "Ingest this" | The Ingest workflow in `AGENTS.md` |
| "Health-check the wiki" | The Lint workflow — orphans, stale, unreconciled contradictions |
| "Why does X keep happening?" | Look in `wiki/patterns/` first — that's what they're for |
| "Research [company]" | `automations/account-researcher.md` |
| "Prep me for my next meeting" | `automations/pre-meeting-prep.md` |
| "Write the team update" | `automations/exec-team-update.md`, team format |
