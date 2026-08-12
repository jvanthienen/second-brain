# Use case: Pre-Meeting Prep

**By 7:30 you'll have:** your own meeting-prep skill and a one-screen brief for a real
upcoming meeting: who is coming, what happened last time, what the meeting must achieve.

---

## Think first: where do your meetings live?

- Your calendar: Outlook or Google. That is where the agent would FIND the meeting.
- Your transcripts: where do they land today? Granola (already files on your Mac), Fireflies
  or Otter (cloud, API key), Teams recaps (copy-paste)?
- Your memory: what do you already know about these people that no system holds?

## Connect it: pick your lane

| Your situation | Do this tonight |
|---|---|
| Granola user | Nothing to connect: your notes are already local files. Point the agent at the folder |
| Fireflies / Otter | They have APIs: an API key connects your transcript history later |
| Teams shop | Open a meeting recap, copy the transcript into a file. Works now |
| Calendar | The connector is one click later; tonight, pasting the invite is faster |

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
