# Northwind Analytics — managed database migration go-live

**Date:** 2026-06-19
**Type:** Transcript (edited for length)
**Attendees:** Daniel Osei (Head of Data Platform), Sofia Marchetti (VP Engineering),
Priya Raman (SE), Sam Rivera
**Duration:** 45 min

---

**Priya:** Cutover finished at 04:20 this morning. All twelve services are on the managed
instance. No rollbacks.

**Daniel:** I'll admit I was expecting to be up all night. It was uneventful, which from where
I sit is the highest possible praise.

**Sofia:** What does this do to the incident numbers?

**Daniel:** The database-related pages were about 40% of our on-call volume. That should mostly
go away. I want a month of data before I claim it publicly, but directionally, yes.

**Sofia:** Good. That was the thing I was most tired of hearing about.

**Sam:** Anything still open from your side?

**Daniel:** One thing, and it's not a migration issue. Our egress costs went up again last
month. It's not enormous but it's the line item that keeps getting flagged in reviews.

**Sam:** Flagged by whom?

**Daniel:** Finance. It comes up every quarter. I don't think anyone believes it's a real
problem, it's just the number that's easiest to point at.

**Priya:** There are a few things we could do architecturally. Regional caching would take the
biggest bite out of it.

**Daniel:** Send me something and I'll take a look.

**Sofia:** Let's get it in front of finance too. If it's the number that keeps coming up, let's
kill it as a topic.

## Actions

- Priya: egress optimization proposal
- Daniel: review, then take to finance
- Sam: include in the September renewal outline

## My read

Best call we've had with this account. Daniel was genuinely positive, which is new. Sofia is
solidly in our corner.

**Egress is clearly the thing finance cares about** — it's come up in three separate
conversations now. If we solve it before the renewal, we take the main objection off the table.
