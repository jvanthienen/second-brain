# Use case: Pre-Meeting Prep

**By 7:30 you'll have:** your own meeting-prep skill and a one-screen brief for a real
upcoming meeting: who is coming, what happened last time, what the meeting must achieve.

---

## Think first: where do your meetings live?

- Your calendar: Outlook or Google. That is where the agent would FIND the meeting.
- Your transcripts: where do they land today? Granola, Fireflies, Otter (they all ship
  MCPs), Teams recaps (WorkIQ MCP, or copy-paste)?
- Your memory: what do you already know about these people that no system holds?

## Connect it: pick your lane

| Your situation | Do this tonight |
|---|---|
| Granola user | Connect the official Granola MCP: two minutes, and your meetings flow in |
| Fireflies / Otter | They ship MCPs too: connect one the same way, or export a transcript tonight |
| Teams shop | Connect the WorkIQ MCP and your meeting history is queryable. Fallback: copy a recap into a file |
| Calendar | The connector is one click later; tonight, pasting the invite is faster |

**How to connect it, the short version (the same moves work for any MCP):**

- **Granola:** Claude Desktop > Settings > Connectors > Add custom connector > paste
  `https://mcp.granola.ai/mcp` > sign in when the browser opens. Test: "list my recent
  Granola meetings." Newer Granola versions encrypt the local cache, so the MCP is the
  reliable lane; copying a transcript out of the app into `raw/_inbox/` always works as a
  fallback.
- **Fireflies / Otter:** same moves with the MCP URL from their docs. No luck? Export one
  transcript into `raw/_inbox/` tonight.
- **Teams:** connect the WorkIQ MCP so your meeting history is queryable. Microsoft folks:
  ask Josefina, she knows the internal ones.
- **On Copilot instead of Claude:** MCPs connect through your company's Copilot setup, not
  a personal settings screen. Ask your agent what is already wired, and ask Josefina on the
  night.
- **Calendar:** paste the invite into the chat tonight. The calendar connector is one click
  later: Settings > Connectors.

Step-by-step recipes for every lane: [`../connect-guide.md`](../connect-guide.md)

## Build your version of the skill

The pro version ships in `automations/pre-meeting-prep.md`. **Don't open it yet.** First
ingest at least one real transcript about the account (Step 2 of WORKSHOP.md), then paste:

> I want to build a pre-meeting-prep skill for my second brain. Interview me first, one
> question at a time: what is my next real external meeting (I will paste the invite:
> subject, time, attendees), what do I want out of it, and where do my transcripts live so
> we can connect or ingest them. Then draft `automations/pre-meeting-prep.md` as a short
> prose playbook, show me, and produce the brief: one screen, who is coming and whether I
> have met them, what happened last time, open threads, the one objective, and three
> questions I should ask. Flag anyone I have never met. Never invent history.

## While it runs

- The two highest-value lines are "NEW: you have never met this person" and any unreconciled
  contradiction involving someone in the room.
- The objective comes from open threads, never invented.
- One screen. If it doesn't fit, it won't get read in the corridor.

## Steal from the pro

Open `automations/pre-meeting-prep.md` (shipped). Did your version surface contradictions?
Match attendees by email domain? Merge what's missing.

## Your 3-minute demo

Show the brief and point at one line the agent could only write because the brain remembers:
a flagged new attendee, a contradiction, a pattern in play. Close with: "it did no new work.
It assembled work already done, at the moment it is useful."
