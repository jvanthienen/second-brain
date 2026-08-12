# Use case: Pipeline Review

**By 7:30 you'll have:** your own pipeline-review skill and your real pipeline reconciled
against what your brain knows: consistent, stale, contradicted, or missing, with drafted
updates you approve one at a time.

---

## Think first: what does your CRM believe, and what do YOU know?

- Which CRM, and who admins it: you, or an IT team?
- Where do the two truths drift apart? The CRM has stages and dates; your head has why.
- What does "stuck" actually mean in your world: days silent, stage age, a missing champion?

## Connect it: pick your lane

| Your situation | Do this tonight |
|---|---|
| Founder / self-admin on HubSpot or Attio | They have official MCPs: connect yours before you build and reconcile LIVE |
| Corporate CRM (Salesforce, Dynamics) | Export open opportunities as CSV now, drop it in `data-pipeline/`. Kick off the IT/MCP request Friday |
| No CRM export handy | List your top 5 deals from memory into a file: stage, value, close date. That is enough to learn on |

Step-by-step recipes for every lane: [`../connect-guide.md`](../connect-guide.md)

## Build your version of the skill

The pro version ships in `automations/pipeline-review.md`. **Don't open it yet.** Ingest a
transcript or two about your accounts first, then paste:

> I want to build a pipeline-review skill for my second brain. Interview me first, one
> question at a time: where is my pipeline data (my CSV is in data-pipeline/ if I have one,
> or help me connect my CRM's MCP), what my stage names mean, and what counts as "stuck" for
> me. Then draft `automations/pipeline-review.md` as a short prose playbook, show me, and
> run it: classify every opportunity as consistent, stale, contradicted, or missing versus
> what the wiki knows, and draft the update comment for anything that needs one, citing the
> wiki page and source date. Do not write to any system. I approve one item at a time.

## While it runs

- The point is drift: your knowledge and your CRM disagree, and by quarter end nobody knows
  which is true.
- If the wiki and CRM disagree, it flags; it does not assume the wiki is right.
- Never batch-approve. Accept, edit, or skip, per item.

## Steal from the pro

Open `automations/pipeline-review.md` (shipped). Compare: did yours cite wiki pages and
source dates in every draft? Merge.

## Your 3-minute demo

Show one CONTRADICTED opportunity and read the drafted comment. Then show the gate: nothing
was written anywhere. Say why: an agent that writes to your CRM unattended will eventually
write something wrong, and you will find out on a forecast call.
