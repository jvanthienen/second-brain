# Second Brain — a working template

An **LLM-maintained wiki** that compounds. Not a note-taking system — a knowledge base where
the agent does the maintenance that humans always abandon.

Based on [Andrej Karpathy's pattern for LLM-built knowledge bases](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f),
instantiated for someone who manages a portfolio of accounts, projects or relationships.

> **All data here is fictional.** Companies, people, numbers and meetings are invented.
> Replace them with your own.
> The customer names are real brands used fictionally, purely so workshop examples feel
> familiar. No affiliation, and nothing here reflects real data about those companies.

> 🎓 **At the workshop?** Start with [`WORKSHOP.md`](WORKSHOP.md).

---

## The idea

Most AI-plus-documents setups are RAG: upload files, retrieve chunks at query time, generate an
answer. It works, but **the LLM rediscovers everything from scratch on every question.** Nothing
accumulates.

This is different. The LLM **incrementally builds and maintains a persistent wiki** that sits
between you and the raw sources. A new source doesn't get indexed — it gets *integrated*.
Entity pages update. Contradictions get flagged. The synthesis strengthens.

```
   RAG                              This
   ─────────────────────            ─────────────────────
   Question                         Question
      ↓                                ↓
   Retrieve chunks                  Read the wiki
      ↓                                ↓
   Synthesize from scratch          Answer already synthesized
      ↓                                ↓
   Answer                           Answer → filed back as a page
      ↓                                ↓
   Nothing kept                     Wiki got richer
```

**The wiki is a compounding artifact.** The cross-references are already there. The
contradictions have already been flagged.

---

## Three layers

| Layer | Where | Who writes it |
|---|---|---|
| **Raw sources** | [`raw/`](raw/) | Nobody — **immutable** |
| **The wiki** | [`wiki/`](wiki/) | **The LLM, entirely** |
| **The schema** | [`AGENTS.md`](AGENTS.md) | You, co-evolved over time |

You never write the wiki. You curate sources, ask good questions, and direct the analysis. The
LLM does the summarizing, cross-referencing, filing and bookkeeping.

> *"Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."*

---

## Three workflows

### Ingest
Drop a source in [`raw/_inbox/`](raw/_inbox/) → *"ingest this"* → the agent reads it, discusses
takeaways, updates **8–15 pages**, flags contradictions, updates index and log.

### Query
Ask a question → the agent reads [`wiki/index.md`](wiki/index.md), drills into pages, answers
with citations. **Good answers get filed back as new pages.**

### Lint
*"Health-check the wiki"* → orphans, stale claims, unreconciled contradictions, concepts that
deserve their own page.

---

## What's in the wiki right now

Six sources ingested, 17 pages, spanning June–August 2026.

```
wiki/
├── index.md          ← catalog — the agent reads this first
├── log.md            ← append-only timeline
├── accounts/         ← what's happening now (3)
├── backgrounders/    ← who they are (2)
├── people/           ← stakeholders worth tracking (6)
├── motions/          ← plays we're running (2)
├── patterns/         ← dynamics seen more than once (2)
├── blockers/         ← specific stuck things (2)
└── companies/        ← competitors, third parties (1)
```

**The interesting pages are the cross-cutting ones.** [[Commitment Flexibility vs Discount Depth]]
didn't come from any single meeting — it emerged from three, at three different accounts, and it
reframes all of them. That's the compounding.

---

## Try it

**1. Query something no single source answers**

> "Why do our commitment deals keep stalling?"

The answer lives in `patterns/`, assembled from three separate meetings across three accounts.

**2. Ingest the waiting source**

> "Ingest the new source in raw/_inbox."

It touches around a dozen pages, contradicts two things the wiki currently treats as settled,
and creates a new page. Watch `wiki/log.md` afterwards.

**3. Lint it**

> "Health-check the wiki. Anything stale, orphaned or contradictory?"

See [`demo/runbook.md`](demo/runbook.md) for a full walkthrough.

---

## Setup

```bash
git clone <your-fork> second-brain
cd second-brain
```

1. Point your agent at [`AGENTS.md`](AGENTS.md) — rename to `CLAUDE.md` for Claude Code, keep as
   `AGENTS.md` for Codex or Copilot CLI.
2. Edit [`BRAIN.md`](BRAIN.md) — replace the fictional persona. **The only required step.**
3. Open the folder in Obsidian. Turn on graph view.
4. Delete the sample content when you're ready, or keep it to practise on.

Full instructions: [`docs/setup.md`](docs/setup.md).

---

## Connectors

Deliberately connector-agnostic. Nothing in `wiki/` knows where mail or chat comes from.

| Layer | Options |
|---|---|
| **Chat** | Slack · Teams · Discord |
| **Mail + calendar** | Gmail · Outlook |
| **Knowledge store** | Local markdown *(default)* · Obsidian · Notion |
| **Numbers** | CSV fixtures *(default)* · your CRM or warehouse |
| **Research** | Web search · contact enrichment · news |

If swapping a connector forces an edit inside `wiki/`, something has leaked across the boundary.

---

## The agents

Built **on top of** the wiki — they read it and write back to it. See
[`automations/`](automations/).

| Agent | What it does |
|---|---|
| Account Researcher | Cold company → Backgrounder + Account page |
| Stakeholder Map | Who matters, who reports to whom, where the gaps are |
| News Watch | Daily scan; surfaces only what changes the plan |
| Pre-Meeting Prep | Calendar → one-screen brief, composed from the wiki |
| Pipeline Review | Reconciles the wiki against CRM. Drafts only. |
| Exec & Team Update | A period of activity → audience-ready summary |
| Daily Capture | 6 PM sweep: your meetings file themselves into the inbox |
| Chief of Staff | Not a skill: the one agent wearing all of the above. Owns memory, rhythm, voice |

---

## Conventions

- **Every claim carries a source and a date.** `(2026-08-07, Sofia Marchetti pre-brief)`
- **Never write `$0` for a number you haven't pulled.** Write `—`. A zero is a claim; a dash is
  an admission.
- **Contradictions are never silently overwritten.** They get a section.
- **A source that touched two pages was under-processed.**
- **Nothing auto-sends.** Agents draft; you review; then it goes.

---

## License

MIT — see [`LICENSE`](LICENSE).
