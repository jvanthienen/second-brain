# Ingesting a source

The core loop. Everything else in this repo exists to support it.

---

## The short version

1. Drop a file in `raw/_inbox/`
2. Say: **"Ingest the new source in raw/_inbox."**
3. Stay involved — read what it proposes, correct it
4. It updates ~8–15 pages, the index, and the log

---

## What good looks like

**A meaningful source touches 8–15 pages.** If it touched two, it was summarized rather than
integrated, and you've lost most of the value.

Worked example — the CFO pre-brief in `raw/_inbox/` should touch:

| Page | What changes |
|---|---|
| `accounts/northwind-analytics` | State of play, two contradictions, threads re-prioritized |
| `people/rachel-kim` | Rewritten — first real intel on the economic buyer |
| `people/tom-bradley` | His June characterization is now known to be wrong |
| `people/daniel-osei` | Flight risk |
| `people/sofia-marchetti` | Confirmed as the highest-value relationship |
| `motions/egress-cost-proposal` | Downgraded — aimed at an objection nobody has |
| `motions/committed-spend-renewal` | Northwind's real blocker identified |
| `patterns/commitment-flexibility-vs-discount-depth` | Northwind promoted from inference to evidence |
| `patterns/champion-dependency-risk` | New instance |
| `companies/vertex-cloud` | Now at two accounts, same entry route |
| `blockers/northwind-marketplace-listing-stalled` | Recommend closing |
| `index.md`, `log.md` | Registration and timeline |

One source. Twelve pages. Two things the wiki believed turn out to be wrong.

---

## Stay involved

Karpathy's advice, and it holds: ingest one at a time and stay in the loop, at least at first.

You know things the source doesn't carry — tone, what someone meant, what was said off the
record. The agent will ask; answer properly.

Batch ingestion works once the schema is mature. Early on it produces a wiki full of confident
mistakes.

---

## Contradictions are the point

The highest-value output of an ingest is not the summary. It's the moment the agent says:

> *"This contradicts what page X has said since June."*

**Never let it silently overwrite.** The `## ⚠️ Contradictions` section is the record of what you
used to believe and why you stopped — and that's often more useful than the current claim.

---

## After ingesting

Check three things:

1. **`wiki/log.md`** — does the entry match what you expected?
2. **The graph view** — did any new connections appear?
3. **Anything that surprised you** — if the agent inferred something you disagree with, correct
   it *and* write the rule into `AGENTS.md` so it doesn't recur.

That third one is how the schema co-evolves. It's the difference between a system that gets
better and one that repeats itself.

---

## Where sources come from

| Source | How |
|---|---|
| Meeting transcripts | Export from your meeting tool |
| Your own notes | Write into `raw/notes/` |
| Articles | Obsidian Web Clipper → markdown |
| News | [News Watch](../automations/news-watch.md) drops material items into `_inbox/` |
| Email threads | Forward, save as markdown |

**Curation is your job.** The agent will faithfully integrate whatever you give it, including
noise.
