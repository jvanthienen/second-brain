# Use case: Exec & Team Update

**By 7:30 you'll have:** your own update skill and this week's update written from what your
brain learned tonight, in a voice you defined in a file, optionally delivered to a real
channel in front of everyone.

---

## Think first: who reads your updates, and where?

- Who is the audience: your working team, your manager, execs? They need different lengths.
- Where do updates land in your world: a Slack channel, a Teams channel, an email thread?
- What does your reader actually want: what happened, or what changed and what you need?

## Connect it: pick your lane

| Your situation | Do this tonight |
|---|---|
| Slack shop | The Slack connector is one click in Claude Desktop: connect it and deliver live |
| Teams shop | Teams connector where available; otherwise draft on screen and paste |
| Email updates | Draft on screen tonight; the mail connector is a later upgrade |
| No connection | The draft on screen IS the demo. Delivery is plumbing |

Step-by-step recipes for every lane: [`../connect-guide.md`](../connect-guide.md)

## Build your version of the skill

The pro version ships in `automations/exec-team-update.md`. **Don't open it yet.** Ingest at
least one real source first so there is something to report, then paste:

> I want to build an update skill for my second brain. Interview me first, one question at a
> time: who reads my updates and where do they land, how often, and what my reader cares
> about most. Have me describe how I like to sound, and read docs/soul.md for the voice
> rules. Then draft `automations/exec-team-update.md` as a short prose playbook, show me,
> and write this week's update from wiki/log.md and the account pages: lead with what
> changed, end with asks that have named owners and dates. Draft only. If I approve and my
> chat is connected, post it where I tell you.

## While it runs

- Contradictions and new patterns are usually the story. A page that changed its mind beats
  a meeting that happened.
- An update with no ask is a status report.
- Two real items beat eight filler ones.

## Steal from the pro

Open `automations/exec-team-update.md` (shipped). Compare: team versus exec versions, the
word caps, "no jargon for execs". Merge what's missing.

## Your 3-minute demo

Read two bullets aloud, then open `docs/soul.md` and point at the rule that shaped them.
That is the moment the room sees the voice is configurable, not generic. If you connected
Slack or Teams, send it to yourself live: a real message in a real system, gated by you.
