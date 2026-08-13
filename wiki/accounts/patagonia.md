# Patagonia

> **Living page — what's happening now.** For who they are, see
> [[Patagonia - Backgrounder]].
>
> **Last reviewed:** 2026-08-05 · **Sources:** 2

---

## The one thing that matters

**[[TWS]] entered through finance, not engineering** — and they sent a VP in week one.
They found the same gap we have: nobody senior on our side has a relationship with the people
who control this budget.

---

## Current state

Fastest-growing account in the book. Consumption has roughly doubled year over year, driven by
model training and inference rather than customer count, which makes it lumpier and
higher-ceiling than [[Nike]].

The technical relationship is excellent and the commercial relationship is thin. There is no
committed agreement — every dollar is discretionary, renegotiable, and currently under attack.

[[Kai Nakamura]] is a real champion and has been candid to the point of telling us how to
compete. He has also been clear that his preference does not decide this.

---

## Commercial

**No commitment agreement.** Pursuing the first one is the primary motion — see
[[Committed-Spend Renewal]].

The blocker is not discount depth. Per [[Kai Nakamura]] (2026-07-08), Ana Petrov will not trade
optionality for a better rate: if model-training demand doubles they would be under-committed,
and if the peak season comes in soft they would be holding a commitment they cannot consume.
She would rather pay more per unit and stay flexible.

This is not unique to them — see [[Commitment Flexibility vs Discount Depth]].

---

## Technical

Demand-forecasting and recommendation model training runs entirely on our GPU capacity. Models
retrain as the catalogue and the season turn over, so consumption scales with model-training
growth rather than revenue.

**Capacity reservation in West through January 2027 is the genuine differentiator.** Kai said
directly that availability matters more than price to him, and that [[TWS]] had no
answer on reserved capacity windows.

Inference optimization work is in flight and has become the competitive response rather than
a cost exercise.

---

## People

| Person | Role here |
|---|---|
| [[Kai Nakamura]] | Head of ML Infrastructure. Champion. Decides the stack in practice, not the budget. |
| Ana Petrov | CTO. Controls budget. **Has never met anyone from our side above the AE.** |
| Mei Lin | Finance Director. Building the cost model. Neutral, wants a defensible number. |
| Jonas Weber | VP Operations. Cares about storefront and fulfilment uptime, not infrastructure. |

---

## Open threads

| Thread | Owner | Status | Next step |
|---|---|---|---|
| First commitment agreement | Josefina | 🟡 Active | Build a flexible structure, not a discount |
| [[TWS]] displacement | Josefina / Priya | 🔴 Urgent | Cost model with Mei + technical response |
| Executive sponsorship | Josefina | 🔴 Not started | Get Ana Petrov in front of a VP this quarter |
| Inference optimization | Priya | 🟡 Accelerated | Proposal review 08-15 |

---

## Risks

- **Single-champion dependency.** [[Kai Nakamura]] is the relationship. See
  [[Champion Dependency Risk]].
- **Active competitive displacement** on training workloads — the most concrete near-term threat
  in the portfolio.
- **No executive coverage.** Two years on the account and their CTO has never met anyone above
  the AE. [[TWS]] closed that gap in a week.
- Fast growth cuts both ways: a soft peak season compresses spend immediately.

---

## Related

[[Patagonia - Backgrounder]] · [[TWS]] ·
[[Commitment Flexibility vs Discount Depth]] · [[Champion Dependency Risk]] ·
[[Committed-Spend Renewal]]
