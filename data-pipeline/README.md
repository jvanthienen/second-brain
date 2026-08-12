# Data pipeline

Where the numbers come from. **Deliberately outside the wiki.**

Ships with CSV fixtures so everything works with no credentials, no network and no auth prompts.

---

## Why numbers aren't in the wiki

From [`../AGENTS.md`](../AGENTS.md):

> **Would you ever filter or compare every account by this?**
> **Yes** → structured data, belongs here. **No** → prose, belongs in a wiki page.

Revenue, contract values, headcounts and dates are all "yes." Restating them in a wiki page
guarantees drift — and worse, a number in a page has no expiry, so an agent will quote it
confidently a quarter later.

Wiki pages carry shape and history. This carries the current figure.

---

## Why fixtures are the default

Not a compromise — the right default for demos and development:

- **Deterministic.** Same answer every run.
- **No auth.** Nothing expires mid-demonstration.
- **Offline.** Conference wifi can't break it.
- **Safe.** No real customer data near a projector.

---

## Files

| File | What's in it |
|---|---|
| `sample-data/consumption.csv` | Monthly consumption per account |
| `sample-data/commitments.csv` | Agreements, terms, drawdown, pace |
| `sample-data/pipeline.csv` | Open opportunities |

All fictional. Note `commitments.csv` has **empty fields** for Patagonia rather than zeros —
they have no agreement, and `0` would be a false claim. See the `$0` rule.

---

## Going live

Replace the fixture reads with real queries. Keep three properties whatever the source:

1. **Every figure carries an "as of" timestamp.** Non-negotiable.
2. **Missing means missing.** Return `null`, never `0`.
3. **Never commit live output.** `.gitignore` already excludes `live/` and `*-live.csv`.

---

## Gotchas worth writing down

Keep this list. Each entry costs someone half a day to rediscover.

**Commitment drawdown is not cumulative consumption.** A commitment only decrements for spend
inside its scope. Prepaid reservations decrement at purchase, not at use. Deriving drawdown by
summing consumption will be wrong in both directions, confidently.

**The current month is an accumulator.** It moves as the source refreshes. Don't compare a
partial month against a complete one without saying so.

**Reported pipeline overstates.** Renewals, superseded opportunities and duplicates all count.
`pipeline.csv` has a `verified` column for exactly this reason — one row is deliberately marked
`no`.

**Watch for silently truncated pages.** Many APIs cap results and return success. A suspiciously
round count usually means a missing continuation token.
