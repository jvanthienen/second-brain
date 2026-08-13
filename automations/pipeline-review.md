# Agent — Pipeline Review

**Trigger:** weekly, Friday 4:00 PM
**Reads:** CRM + `wiki/` + calendar
**Writes:** **draft updates only — never writes to CRM unattended**
**Runtime:** 3–5 minutes

---

## What it does

Reconciles what the wiki knows against what the CRM believes, then drafts the updates. You
approve each one.

The problem it solves isn't writing CRM notes. It's that **your knowledge and your CRM drift
apart**, and by quarter end nobody can tell which is true.

Because the wiki carries *why* things are happening, the drafts are meaningfully better than
anything derived from meeting notes alone.

---

## Process

### 1. Pull CRM state
Every open opportunity: stage, value, close date, last activity, last comment.

### 2. Read the wiki
Account pages, open threads, blockers, and any contradiction recorded since the last run.

### 3. Reconcile

| Signal | Meaning |
|---|---|
| 🟢 **Consistent** | CRM matches the wiki. No action. |
| 🟡 **Stale** | No activity 14+ days. Needs a comment or a date change. |
| 🔴 **Contradicted** | The wiki disagrees with CRM. |
| ⚪ **Missing** | Real activity in the wiki with no opportunity attached. |

### 4. Draft
For each item needing an update, write the comment you'd write: what changed, what's next, what
would move it. **Cite the wiki page and the source date.**

### 5. Review, one at a time
**Accept / Edit / Skip.** Never batch-apply.

---

## Output

```
📊 Pipeline review — week ending 8 Aug

🔴 CONTRADICTED (2)

  Nike — renewal · $12.0M · Stage: Proposal
    CRM close date 2026-08-31 has passed with no stage change.
    Wiki: [[Nike]] — decision expected end of Q3, and the
    cost review is a live competitive benchmark (2026-08-07 pre-brief).
    → Draft: "Renewal timeline moved to end of Q3. Cost-optimization review
       confirmed as a competitive benchmark against TWS, running
       since May. Buyer priority is commitment structure, not discount.
       Next: rebuild proposal around term flexibility."
    → Also suggests: close date → 2026-09-30
    [Accept] [Edit] [Skip]

  Patagonia — first commitment · $2.1M · Stage: Qualify
    Wiki shows an active competitive displacement; stage says Qualify.
    Wiki: [[Patagonia]], [[TWS]] (2026-08-04).
    → Draft: "Competitive pressure confirmed on training workloads. Champion
       prefers to stay; commercial case not built. Blocker is commitment
       shape, not price — see the flexibility pattern. Recommend re-stage
       to Develop."
    [Accept] [Edit] [Skip]

🟡 STALE (1)

  Nordstrom — analytics migration · $0.8M · last activity 21 days
    → Draft: "Validation gate 2 passed 07-30; decision moved to end of
       September. Blocker is the data team's incumbent preference — one of
       three objections is factually wrong and answerable."
    [Accept] [Edit] [Skip]

⚪ MISSING (1)

  [[Egress Cost Proposal]] has no CRM opportunity and was just downgraded.
    → Suggest: no action. Flagging so it isn't silently forgotten.
    [Review]

🟢 CONSISTENT (3) — no action
```

---

## Rules

- **Never write to CRM without explicit per-item approval.** Not "approve all."
- **Every draft cites its wiki page and source date.**
- **Never change a value you can't justify.** Suggest, explain, let the human decide.
- **Preserve history.** Add comments; don't overwrite.
- **If the wiki and CRM disagree, flag it — don't assume the wiki is right.** Sometimes the CRM
  is correct and the wiki is stale. That's a lint finding.

---

## Demo notes

Pre-bake this one. It needs a CRM connection and a week of real activity, neither of which
survives a live demo.

The lesson isn't the automation, it's the **gate.** Show the Accept/Edit/Skip loop and say why
it exists: an agent that writes to your CRM unattended will eventually write something wrong,
and you won't find out until a forecast call. Audiences are visibly reassured when you raise
this before they do.
