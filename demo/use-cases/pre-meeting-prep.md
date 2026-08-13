# Use case: Pre-Meeting Prep

**By 7:30 you'll have:** your own meeting-prep skill and a one-screen brief for a real
upcoming meeting: who is coming, what happened last time, what the meeting must achieve.

---

## Think first: where do your meetings live?

- Your calendar: Outlook or Google. That is where the agent would FIND the meeting.
- Your transcripts: where do they land today? Granola, Fireflies, Otter (they all ship
  MCPs), Teams recaps (Microsoft 365 connector, WorkIQ MCP, or copy-paste)?
- Your memory: what do you already know about these people that no system holds?

## Connect it: pick your lane

| Your situation | Do this tonight |
|---|---|
| Granola user | Connect the official Granola MCP: two minutes, and your meetings flow in |
| Fireflies / Otter | They ship MCPs too: connect one the same way, or export a transcript tonight |
| Teams shop | Microsoft 365 connector in Claude, or the WorkIQ MCP. Fallback: copy a recap into a file |
| Calendar | Built-in connector: connect it FIRST, one click in Settings > Connectors |

**How to connect it:**

**Calendar (do this first, it is a built-in connector):**

1. Claude Desktop > **Settings > Connectors**.
2. Find **Google Calendar**, or **Microsoft 365** for Outlook calendar > **Connect**.
   Sign in and approve in the browser (Microsoft 365 needs your WORK account).
3. Test: "what is my next external meeting?"
4. Sign-in blocked on an admin approval screen? Paste the invite into the chat tonight:
   subject, time, attendees. Send the IT request Friday.

**Granola (every MCP below connects with these same moves):**

1. Claude Desktop > **Settings > Connectors > Add custom connector**.
2. Paste `https://mcp.granola.ai/mcp`.
3. Sign in when the browser opens.
4. Test: "list my recent Granola meetings."

Newer Granola versions encrypt the local cache, so the MCP is the reliable lane. Fallback:
copy a transcript out of the app into `raw/_inbox/`.

**Fireflies / Otter:**

1. Same four moves, with the MCP URL from their docs.
2. No luck? Export one transcript into `raw/_inbox/` tonight.

**Teams:**

1. In Claude: connect the **Microsoft 365** connector (Settings > Connectors > Microsoft
   365 > Connect, work account) and your Teams chats and meetings become readable.
2. On Copilot: connect the WorkIQ MCP, same moves as Granola. Microsoft folks: ask
   Josefina, she knows the internal ones.
3. Fallback: open the meeting recap, copy the transcript into a file in `raw/_inbox/`.

**On Copilot instead of Claude:**

1. MCPs connect through your company's Copilot setup, not a personal settings screen. Ask
   your agent what is already wired, and ask Josefina on the night.

Step-by-step recipe for every connection: [buildergeneralist.com/second-brain](https://www.buildergeneralist.com/second-brain)

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
