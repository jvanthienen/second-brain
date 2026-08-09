# Agent — News Watch

**Trigger:** scheduled — weekdays 7:00 AM
**Reads:** web + `wiki/`
**Writes:** chat digest — and drops genuinely material items into `raw/_inbox/`
**Runtime:** 2–5 minutes

---

## What it does

Scans the news for every account in the book and surfaces **only what changes your plan.**

The hard part isn't finding news. It's not sending you any. A digest that arrives every morning
with something in it gets muted within a week.

---

## Process

### 1. Build the watch list
Every account in [`BRAIN.md`](../BRAIN.md), their key people from `wiki/people/`, and any
competitor with a page in `wiki/companies/`.

### 2. Scan
Last 24 hours: news, funding and M&A, executive moves, filings, outages, engineering blogs,
competitor announcements.

### 3. Filter hard
For each item: **does this change what I would do this week?**

| Include | Skip |
|---|---|
| Funding, acquisition, public-offering movement | Product marketing |
| Executive change in your buying centre | Award wins |
| Public cost or reliability complaints | Routine press releases |
| A competitor with a page targeting your account | Generic industry commentary |
| Layoffs, restructuring, spend freeze | Conference speaking slots |
| **Anything contradicting a wiki page** | Reposts of last week |

**Default to skipping.**

### 4. Connect it to the wiki
Don't relay the headline. State what it means for your position, citing the relevant page. This
is the difference between an alert and an assistant.

### 5. Route it
- **Material enough to change a page** → write it to `raw/_inbox/` as a source and flag it for
  ingest. Don't ingest unattended.
- **Worth knowing, not page-changing** → digest only.
- **Nothing passed the filter** → **send nothing.**

---

## Output

```
📰 Account news — Tuesday 9 Aug

🔴 Tailspin Robotics — competitive
   Vertex Cloud announced GPU price cuts targeting robotics workloads,
   effective September 1.
   → Same workload under pressure since May. Confirms the pricing posture in
     [[Vertex Cloud]] and makes Priya's inference proposal (review 08-15)
     time-critical.
   → Dropped to raw/_inbox/ — recommend ingest.
   → Source: [link] · Confidence: high

🟡 Northwind Analytics — leadership
   CFO Rachel Kim spoke on "infrastructure cost discipline" ahead of a public
   offering.
   → First public signal of her priorities. [[Rachel Kim]] currently has almost
     nothing on it. Useful before the QBR.
   → Source: [link] · Confidence: high

Relecloud Media — nothing of note.
```

---

## Rules

- **Silence is a valid output.** Never manufacture relevance to justify a run.
- **Always link the source.**
- **Flag contradictions loudly.** If news contradicts a page, say which page.
- **Never ingest unattended.** Drop it in `_inbox/` and let a human trigger it.

---

## Demo notes

Hard to demo live — you can't schedule real news for 2 PM on a Thursday. Pre-run it that morning,
or point it at a large public company where something is reliably happening.

Worth saying: **the filter is the product.** Anyone can pipe a news API into a chat channel.
Deciding what *not* to send is the part that requires knowing your book.
