# Tailspin Robotics

> **Living page — what's happening now.** For who they are, see
> [[Tailspin Robotics - Backgrounder]].
>
> **Last reviewed:** 2026-08-05 · **Sources:** 2

---

## The one thing that matters

**[[Vertex Cloud]] entered through finance, not engineering** — and they sent a VP in week one.
They found the same gap we have: nobody senior on our side has a relationship with the people
who control this budget.

---

## Current state

Fastest-growing account in the book. Consumption has roughly doubled year over year, driven by
model training and inference rather than customer count, which makes it lumpier and
higher-ceiling than [[Northwind Analytics]].

The technical relationship is excellent and the commercial relationship is thin. There is no
committed agreement — every dollar is discretionary, renegotiable, and currently under attack.

[[Kai Nakamura]] is a real champion and has been candid to the point of telling us how to
compete. He has also been clear that his preference does not decide this.

---

## Commercial

**No commitment agreement.** Pursuing the first one is the primary motion — see
[[Committed-Spend Renewal]].

The blocker is not discount depth. Per [[Kai Nakamura]] (2026-07-08), Ana Petrov will not trade
optionality for a better rate: if the fleet doubles they would be under-committed, and if the
logistics contract falls through they would be holding a commitment they cannot consume. She
would rather pay more per unit and stay flexible.

This is not unique to them — see [[Commitment Flexibility vs Discount Depth]].

---

## Technical

Vision-model training runs entirely on our GPU capacity. Retraining happens per deployment site,
so consumption scales with fleet growth rather than revenue.

**Capacity reservation in West through January 2027 is the genuine differentiator.** Kai said
directly that availability matters more than price to him, and that [[Vertex Cloud]] had no
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
| Jonas Weber | VP Operations. Cares about robot uptime, not infrastructure. |

---

## Open threads

| Thread | Owner | Status | Next step |
|---|---|---|---|
| First commitment agreement | Sam | 🟡 Active | Build a flexible structure, not a discount |
| [[Vertex Cloud]] displacement | Sam / Priya | 🔴 Urgent | Cost model with Mei + technical response |
| Executive sponsorship | Sam | 🔴 Not started | Get Ana Petrov in front of a VP this quarter |
| Inference optimization | Priya | 🟡 Accelerated | Proposal review 08-15 |

---

## Risks

- **Single-champion dependency.** [[Kai Nakamura]] is the relationship. See
  [[Champion Dependency Risk]].
- **Active competitive displacement** on training workloads — the most concrete near-term threat
  in the portfolio.
- **No executive coverage.** Two years on the account and their CTO has never met anyone above
  the AE. [[Vertex Cloud]] closed that gap in a week.
- Fast growth cuts both ways: a funding or contract delay compresses spend immediately.

---

## Related

[[Tailspin Robotics - Backgrounder]] · [[Vertex Cloud]] ·
[[Commitment Flexibility vs Discount Depth]] · [[Champion Dependency Risk]] ·
[[Committed-Spend Renewal]]
