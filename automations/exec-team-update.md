# Agent — Exec & Team Update

**Trigger:** weekly (team) · monthly (exec) — or on demand
**Reads:** `wiki/` + `wiki/log.md` + calendar
**Writes:** **draft only** — chat post or email, sent by you
**Runtime:** 2–4 minutes

---

## What it does

Turns a period of activity into an audience-ready update. Two different outputs from the same
evidence:

| | **Team update** | **Exec update** |
|---|---|---|
| Audience | Your working team | Leadership |
| Cadence | Weekly | Monthly |
| Length | ~200 words | ~150 words |
| Focus | What happened, who owes what | What changed, what you need |
| Includes | Task assignments | Asks and decisions only |

The mistake almost everyone makes is sending the team version to executives. More detail reads
as less clarity.

---

## Process

### 1. Read the log
`wiki/log.md` is the fastest way to see what actually changed in the period —
`grep "^## \[" log.md | tail -10`. Ingests, new pages, contradictions flagged.

### 2. Find the story
Not a list of events — the two or three things that moved. Ask: what would leadership be annoyed
to learn late? What does the team need to act on Monday?

**Contradictions and new Patterns are usually the story.** A page that changed its mind is more
newsworthy than a meeting that happened.

### 3. Write to the format
Use the matching spec in [`../playbooks/`](../playbooks/) — read
[`../docs/soul.md`](../docs/soul.md) first. **Default to the short version.**

### 4. Pull the asks forward
Named owner, specific request, real date. An update with no ask is a status report.

### 5. Draft — never send

---

## Output — team update

```
📌 Weekly — Josefina's accounts · week ending 8 Aug

WHAT MOVED
• Nike — the cost review isn't routine. It's a live benchmark against
  Vertex Cloud, running since May. We were told in June it was internal.
• Nike — Rachel Kim's actual priority is commitment structure, not
  price. Our egress proposal was aimed at the wrong objection.
• Patagonia — Vertex confirmed. Same finance-first entry as Nike.

WHAT'S STUCK
• Nordstrom migration — one of Fatima's three objections is factually wrong
  and we still haven't demonstrated the counter-example.
• Nike marketplace listing — nobody on their side is asking for it.
  Recommend we stop carrying it.

ASKS
• @Priya — hold egress, prioritise the Patagonia inference proposal by Thu 14th.
• @Priya — demo the materialization equivalent to Fatima before the 20th.
• @Marcus — before more marketplace effort, can we confirm anyone wants it?
```

---

## Output — exec update

```
Monthly — West / Emerging Enterprise · July

The same competitor is now at two of three accounts, and both times entered
through finance.

Nike ($12M renewal, March) — the cost review we were told was routine is
a competitive benchmark that has been running since May. Their CFO wants term
flexibility while every multi-year obligation is under board review, not a
discount. Rebuilding the proposal accordingly. She joins the next QBR — our first access to her.

Patagonia (fastest growth, no commitment) — Vertex approached their finance
director and sent a VP in week one. Our champion prefers us but doesn't own the
budget. Their CTO has never met anyone from our side above the AE.

The pattern across both: we are single-threaded into engineering, and the
competitor is going straight to the people who sign.

ASK: an executive sponsor for Patagonia this quarter, and a commitment
structure other than multi-year flat. The second one affects all three
accounts.
```

---

## Rules

- **Lead with what changed**, not what you did.
- **Every update ends with an ask.**
- **Never send automatically.**
- **No internal jargon in exec updates.** If it needs a glossary, rewrite it.
- **Two real items beat eight filler ones.**

---

## Demo notes

Good closer — it produces something tangible, in your voice, that lands in a real channel.

Run it live and send it to yourself. Most chat tools have a self-message channel; it's a real
API call with no recipients to worry about.

Then show [`../docs/soul.md`](../docs/soul.md) and point out the tone came from a file. That's
the moment the audience sees the output is configurable rather than generic — the most
transferable idea in the session.
