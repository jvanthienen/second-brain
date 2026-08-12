# Automations — the agents

These sit **on top of the wiki**. They read it, and they write back into it — which means every
run makes the wiki richer rather than producing a throwaway artifact.

That's the important distinction. An agent that generates a brief and forgets it is a tool. An
agent that generates a brief *and files what it learned* is part of the brain.

---

## The set

| Agent | Trigger | Reads | Writes |
|---|---|---|---|
| [Account Researcher](account-researcher.md) | On demand | Web | `wiki/backgrounders/`, `wiki/accounts/` |
| [Stakeholder Map](stakeholder-map.md) | On demand | Web + enrichment | `wiki/people/` |
| [News Watch](news-watch.md) | Daily 7:00 AM | Web + `wiki/` | Chat digest, + `raw/_inbox/` if material |
| [Pre-Meeting Prep](pre-meeting-prep.md) | 30 min before | Calendar + `wiki/` | Chat brief |
| [Pipeline Review](pipeline-review.md) | Weekly Fri 4 PM | CRM + `wiki/` | **Drafts only** |
| [Exec & Team Update](exec-team-update.md) | Weekly / monthly | `wiki/` + calendar | **Drafts only** |
| [Daily Capture](daily-capture.md) | Daily 6:00 PM | Your meetings folder | `raw/_inbox/` + digest |
| [Chief of Staff](chief-of-staff.md) | Always | Everything | The role that runs all of the above |

---

## How they compose

```
   Account Researcher ──→ Backgrounder + Account page ──┐
   Stakeholder Map    ──→ Person pages ─────────────────┤
   News Watch         ──→ raw/_inbox/ ──→ ingest ───────┤
                                                        ↓
                                                  THE WIKI
                                                        ↓
                        ┌───────────────────────────────┼──────────────────┐
                        ↓                               ↓                  ↓
                Pre-Meeting Prep              Pipeline Review      Exec & Team Update
```

Everything flows through the wiki. Nothing talks directly to anything else — which is why you
can add a seventh agent without touching the first six.

---

## Rules for all of them

**1. Nothing auto-sends.** Every outbound path stops at draft.

**2. Every claim carries a source and a date.** Unsourced claims are how a wiki quietly rots.

**3. Read [`../AGENTS.md`](../AGENTS.md) before writing to `wiki/`.** Page types, structure and
the contradiction rule apply to agent writes exactly as they do to manual ingest.

**4. Prefer updating an existing page to creating a new one.** New pages are for genuinely new
entities, not for new information about existing ones.
