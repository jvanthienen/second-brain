# Setup

About 30 minutes to a working brain.

---

## 1. Clone and point your agent at the schema

```bash
git clone <your-fork> second-brain
cd second-brain
```

| Agent | Do this |
|---|---|
| Claude Code | `cp AGENTS.md CLAUDE.md` |
| Codex / Copilot CLI | Already named correctly |
| Other | Point it at `AGENTS.md`, or paste it at the start of a session |

**This is the step that makes it work.** Without the schema the agent is a chatbot with file
access; with it, it's a disciplined wiki maintainer.

---

## 2. Make `BRAIN.md` yours — *required*

Replace the fictional persona. An agent reading someone else's context gives you someone else's
answers.

Minimum: identity, mandate, operating model, portfolio. **Spend time on the operating model** —
it shapes every answer.

---

## 3. Open it in Obsidian

Point Obsidian at the repo root and **turn on graph view.**

This isn't cosmetic. The graph is how you see whether the wiki is actually connected or just a
pile of files — hub pages, orphans, and clusters are all visible at a glance.

---

## 4. Try it before you change anything

The sample wiki has six sources ingested and one waiting. Before replacing it, run the three
workflows so you know what "working" feels like:

```
"Why do our commitment deals keep stalling?"     ← query across pages
"Ingest the new source in raw/_inbox."           ← watch it touch ~12 pages
"Health-check the wiki."                         ← lint
```

See [`../demo/runbook.md`](../demo/runbook.md).

---

## 5. Make it yours

```bash
rm -rf wiki/* raw/transcripts/* raw/notes/*
```

Then either drop your own sources into `raw/_inbox/` and ingest them one at a time, or run
[Account Researcher](../automations/account-researcher.md) to bootstrap Backgrounders from
public information.

**Ingest one source at a time at first.** Watch what the agent does, correct it, and write the
corrections into `AGENTS.md`. That's the co-evolution the pattern depends on — after five or six
sources the schema will fit your domain far better than anything you could have specified up
front.

---

## 6. Connect your tools

Nothing is required to start. The wiki works offline.

| Connector | Needed for |
|---|---|
| Web search | Account Researcher, News Watch |
| Chat (Slack/Teams) | Exec & Team Update |
| Mail + calendar | Pre-Meeting Prep |
| Contact enrichment | Stakeholder Map |
| CRM | Pipeline Review |

Copy `.env.example` to `.env`. **It's gitignored — keep it that way.**

---

## Troubleshooting

| Symptom | Cause |
|---|---|
| Generic answers, ignores the wiki | Schema not loaded. Check the `AGENTS.md` / `CLAUDE.md` filename. |
| Ingest touches 2 pages, not 12 | Agent is summarizing, not integrating. Point it back at the Ingest workflow. |
| Silently overwrites instead of flagging contradictions | The highest-value rule in the schema. Re-read that section together. |
| Pages full of numbers | The "would you filter all accounts by this?" test isn't being applied. |
| Everything is an orphan | It's not adding `[[wikilinks]]`. Check the Cross-links section. |
| Wrong voice | `docs/voice.md` not being read, or too vague to act on. |
