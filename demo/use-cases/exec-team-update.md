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
| Teams shop | Claude connects via the Microsoft 365 connector (Teams chats + channels); Copilot talks to Teams natively |
| Email updates | Draft on screen tonight; the mail connector is a later upgrade |
| No connection | The draft on screen IS the demo. Delivery is plumbing |

**How to connect it:**

**Slack:**

1. Claude Desktop > **Settings > Connectors**.
2. Find Slack > **Connect**. Sign in to YOUR workspace in the browser and approve.
3. Test: "post 'test' to my own DM in Slack." Delete the test after.

**Teams from Claude (the Microsoft 365 connector):**

1. Claude Desktop > **Settings > Connectors**.
2. Find Microsoft 365 > **Connect**. Sign in with your WORK Microsoft account (personal
   @outlook.com accounts do not work).
3. Test: "list my Teams channels."

Available on every Claude plan, but a Microsoft Entra admin has to grant a one-time
consent. If sign-in dies on an approval screen, that is the IT request to send Friday;
tonight, draft on screen and paste.

**Teams with Copilot:**

1. Nothing to connect: Copilot already talks to Teams.
2. Ask it to draft your update, review it, then have it post to your team channel. No
   copy-paste.

**Before you build (any lane):**

1. Ingest at least one real meeting so there is something to report.
2. Dig up 2 or 3 past updates you were proud of and paste them in: the skill learns voice
   and structure from real examples, not from adjectives.

Step-by-step recipes for every lane: [buildergeneralist.com/second-brain](https://www.buildergeneralist.com/second-brain)

## Build your version of the skill

The pro version ships in `automations/exec-team-update.md`. **Don't open it yet.** Ingest at
least one real source first so there is something to report, then paste:

> I want to build an update skill for my second brain. Interview me first, one question at a
> time: who reads my updates and where do they land, how often, and what my reader cares
> about most. Have me describe how I like to sound, and read docs/soul.md for the voice
> rules. Ask me to paste two or three past updates I was proud of, and learn the voice and
> structure from those real examples. Then draft `automations/exec-team-update.md` as a
> short prose playbook, show me,
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
