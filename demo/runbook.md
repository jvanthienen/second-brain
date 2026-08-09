# Demo runbook

A 20-minute walkthrough that shows the brain **working**, not just existing.

**The arc:** show the payoff → open the hood → show it compound → show it catch you being wrong.

> Have Obsidian open on this folder with graph view visible. It does more persuasive work than
> anything you'll say.

---

## Before you start

- [ ] Obsidian open on the repo root, graph view on a second monitor or tab
- [ ] Agent session open, pointed at `AGENTS.md`
- [ ] `raw/_inbox/2026-08-07-northwind-cfo-prebrief.md` still un-ingested
- [ ] `wiki/log.md` open in a tab — you'll come back to it
- [ ] A recording of Act 3 as backup, in case the live ingest misbehaves

---

## Act 1 — the payoff (3 min)

Don't explain anything first. Just ask:

> **"Why do our commitment deals keep stalling?"**

The agent reads `wiki/index.md`, finds [[Commitment Flexibility vs Discount Depth]], and answers
with a portfolio-level insight: three accounts, three apparently different problems, one shared
cause — customers are declining commitments to preserve optionality, and we keep answering with
discount depth.

**The line to land:** *"That answer isn't in any meeting I had. It emerged from three of them,
at three different accounts, weeks apart."*

---

## Act 2 — open the hood (4 min)

Now show them it's just files.

1. **`raw/`** — "Six meeting transcripts. Immutable. The agent reads these and never edits them."
2. **`wiki/`** — "The agent wrote every one of these. I've never edited a page by hand."
3. **`AGENTS.md`** — "This is the whole configuration. It's prose. It tells the agent how to
   maintain the wiki." Scroll to the page types and the contradiction rule.
4. **Graph view** — hover [[Commitment Flexibility vs Discount Depth]] and show it connecting
   three accounts.

**The line:** *"Three layers. Sources it can't touch, a wiki it owns completely, and a schema I
control. That separation is the whole design."*

---

## Act 3 — watch it compound (8 min) ⭐

This is the demo. Everything else is setup.

> **"Ingest the new source in raw/_inbox."**

Narrate while it works. It should:

| # | What it does | Why it matters |
|---|---|---|
| 1 | Read the pre-brief | — |
| 2 | **Flag contradiction #1** — the cost review isn't routine, it's a live competitive benchmark against [[Vertex Cloud]] since May | We were told in June it was routine. We believed it for two months. |
| 3 | **Flag contradiction #2** — nobody in finance cares about egress | We've been building the wrong proposal since June |
| 4 | Update [[Northwind Analytics]] — state of play, contradictions, threads | |
| 5 | Substantially rewrite [[Rachel Kim]] — first real intel on the economic buyer | |
| 6 | **Create [[Daniel Osei]] risk note** — he's interviewing elsewhere | New instance of [[Champion Dependency Risk]] |
| 7 | Update [[Vertex Cloud]] — now at **two** accounts, same finance-first entry | The pattern hardens |
| 8 | Strengthen [[Commitment Flexibility vs Discount Depth]] — Northwind moves from *inference* to *evidence* | The open question from the last lint gets closed |
| 9 | Downgrade [[Egress Cost Proposal]] and [[Northwind Marketplace Listing Stalled]] | |
| 10 | Update `index.md` and append to `log.md` | |

**Then open `wiki/log.md`** and show the new entry next to the previous six.

**The line:** *"One source. Twelve pages. And it just told me that two months of work was aimed
at an objection the buyer never had."*

> **Why this lands:** it's not summarization. The agent connected a claim from June to a
> contradiction in August across two different documents, and concluded the team has been
> solving the wrong problem. That's the moment people stop seeing a file system.

---

## Act 4 — the compounding closes a loop (3 min)

Re-run the Act 1 question:

> **"Why do our commitment deals keep stalling?"**

The answer is now stronger — Northwind has moved from inference to confirmed evidence, with the
public-offering reason attached.

Then:

> **"File that as a new page."**

**The line:** *"Explorations compound too. That analysis is now part of the wiki, so the next
question starts from here instead of from scratch."*

---

## Act 5 — lint (2 min, optional)

> **"Health-check the wiki."**

Orphans, stale pages, unreconciled contradictions, concepts that deserve their own page.

**The line:** *"This is the maintenance nobody does. It's why wikis die. It costs nothing here."*

---

## If you have more time

| Add | Shows |
|---|---|
| Pre-Meeting Prep agent | The wiki composing into something operational |
| Stakeholder Map | Best visual after the graph |
| Exec update → send to your own chat | It takes real action in a real system |

---

## Questions you will get

**"How is this different from RAG / NotebookLM?"**
RAG retrieves and re-synthesizes on every query. Nothing accumulates. Here the synthesis is
written down, cross-referenced, and improves with each source. Act 4 is the proof.

**"What stops it writing something wrong?"**
Three things: contradictions are surfaced rather than overwritten, every claim carries a source
and date, and nothing auto-sends. It also gets things wrong sometimes — the log makes that
visible and reversible.

**"How long did this take to build?"**
The schema is one prose file. The wiki wrote itself from six sources. The honest answer is that
the hard part was deciding the page types, not the tooling.

**"Does this work with Slack / Notion / [their tool]?"**
Yes — the knowledge layer never names a vendor. Show the connector table in `README.md`.

**"What happens at 500 pages?"**
`index.md` stops being enough and you add a search tool. Karpathy names `qmd` for this. Below a
few hundred pages, the index file genuinely works.
