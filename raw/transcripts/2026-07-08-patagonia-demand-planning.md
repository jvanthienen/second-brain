# Patagonia — demand planning

**Date:** 2026-07-08
**Type:** Transcript (edited)
**Attendees:** Kai Nakamura (Head of ML Infrastructure), Priya Raman (SE), Josefina Van Thienen
**Duration:** 50 min

---

**Kai:** We're going to need more headroom by October. Model training is growing faster than we
modelled and every new market we launch in means retraining the demand-forecasting and
recommendation models on that region's data.

**Priya:** How much more?

**Kai:** Call it 40% over current. Maybe more if the personalization rollout lands.

**Josefina:** We can reserve capacity in West through January. That gives you scheduling certainty
through the peak.

**Kai:** That's exactly what I want. The thing that actually hurts us isn't price, it's not
being able to get the hardware when we need it. Last year we lost three weeks waiting.

**Josefina:** Understood. Have you thought about a committed agreement? It would lock in both the
capacity and the rate.

**Kai:** Ana won't sign a multi-year commitment right now. She's been clear about it.

**Josefina:** Is that a price thing?

**Kai:** No. It's that we can't forecast what we'll need in two years. If model training doubles
we'd be under-committed and if peak season comes in soft we'd be sitting on a commitment we
can't use. She'd rather pay more per unit and stay flexible.

**Priya:** Even with a meaningful discount?

**Kai:** I've heard her say the discount isn't worth the lock-in. She's said it more than once.

**Josefina:** That's useful to know.

**Kai:** For what it's worth, I'd sign something. I'd rather have the certainty. But it's not my
budget.

## Actions

- Josefina: reserve West capacity through January
- Priya: model the October requirement
- Josefina: think about what a flexible commitment structure would look like

## My read

The capacity reservation is a genuine differentiator — Kai said explicitly that availability
matters more than price to him.

**The commitment blocker is flexibility, not discount depth.** Ana won't trade optionality for a
better rate. Our standard three-year flat structure is the wrong shape for this account, and I
don't currently have another one to offer.
