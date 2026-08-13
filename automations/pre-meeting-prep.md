# Agent — Pre-Meeting Prep

**Trigger:** 30 minutes before any external meeting
**Reads:** calendar + `wiki/` + recent mail and chat
**Writes:** chat brief to you, plus a one-page backgrounder file in `briefs/`
**Runtime:** 1–3 minutes

---

## What it does

Produces two artifacts for the same meeting:

1. **The brief** — one screen of judgment: who's coming, what happened last time, what's
   open, what you should be trying to achieve. Lives in chat (and, on request, a team
   channel). This is the thing you read in the corridor.
2. **The backgrounder** — a one-pager saved in `briefs/`, meant to travel: everyone
   attending (role, coverage, whether we've met), the goals for the meeting, the key
   points, and what we learned most recently, numbered. Share it as an attachment so the
   whole team walks in with the same page. Export to PDF before sharing outside chat.

**This is the agent that makes the wiki feel worth it**, because it does no new work — it
assembles work already done, at the moment it's useful. That's the demo where people stop
watching a tool and start seeing a system.

---

## Process

### 1. Find the meeting
Next external event on the calendar. Skip internal-only unless asked.

### 2. Match it to an account
Attendee email domain first, then title, then organizer. **If no match, say so** and fall back
to a live [Account Researcher](account-researcher.md) pass — an unmatched external meeting is
often the most important one.

### 3. Assemble from the wiki
- **Attendees** — pull their Person pages. Role, coverage, whether you've met. **Flag anyone
  new.**
- **The one thing that matters** — straight from the top of the Account page.
- **Last contact** — most recent source in `raw/` for this account.
- **Open threads** — from the Account page, filtered to these attendees.
- **Contradictions** — if the Account page has an unreconciled contradiction relevant to who's
  in the room, surface it. This is often the highest-value line.
- **Patterns** — if this account is an instance of an active Pattern, say so.

### 4. Set the objective
The one thing this meeting should achieve, and what would make it a wasted hour. Derive it from
open threads; don't invent it.

### 5. Suggest questions
Three or four, tied to open threads and to what the wiki says you don't know.

### 6. Write the backgrounder
Save `briefs/YYYY-MM-DD-<account>-<meeting>-backgrounder.md`, one page, four sections:

- **Who is in the room** — every attendee with role, relationship strength, and a one-line
  read on how they decide (pull from Person pages; never invent).
- **Goals** — the objective from step 4, plus what would make the meeting a wasted hour.
- **Key points** — the 3-5 things the team must hold in their heads walking in.
- **What we just learned** — the most recent intel, numbered, newest source first. Respect
  confidentiality marks: off-the-record detail stays out of anything that travels.

---

## Output

```
📋 Nike — QBR
   Tomorrow 10:00 AM · 60 min · 4 attendees

THE ONE THING
  We have no relationship with the person who signs the renewal.
  She is in the room for the first time.

WHO
  Sofia Marchetti  VP Engineering        ✅ Strong   champion
  Daniel Osei      Head of Data Platform ✅ Strong   technical DM
  Tom Bradley      Procurement           🟡 Weak     met once, June
  Rachel Kim       CFO                   🔴 NEW      economic buyer

⚠️ UNRECONCILED
  Tom said the cost review was routine (June). Sofia says it's a live
  benchmark against TWS, running since May. Tom is in this room.
  Do not repeat the June framing back to anyone.

OPEN THREADS
  🟡 Renewal terms — the reason this meeting exists
  🟡 Egress proposal — downgraded; Rachel has never mentioned it
  🔴 Marketplace listing — nobody at Nike is asking for it

PATTERN IN PLAY
  Commitment Flexibility vs Discount Depth — she wants term structure,
  not a bigger discount. Do not lead with price.

OBJECTIVE
  A relationship, not a close. Wasted hour = talking only to Sofia and
  Daniel because it's comfortable.

QUESTIONS
  1. (Rachel) How are you thinking about commitment structure ahead of
     next year?
  2. (Rachel) What would make this an easy renewal from where you sit?
  3. (Daniel) Where did the June migration land against your targets?
  4. (Tom) What does the approval calendar look like from here?
```

---

## Rules

- **Flag anyone you haven't met.** The most valuable line in the brief.
- **Surface unreconciled contradictions** when someone in the room is a party to them.
- **Never invent history.** No record of a prior meeting means say so.
- **Numbers must be live or dashed.** This is the moment you're most likely to repeat one aloud.
- **One screen.** If it doesn't fit, it won't get read in the corridor.

---

## Demo notes

**Run this live.** Stage a calendar event with realistic attendees beforehand.

The moment that lands is the `🔴 NEW` line combined with the `⚠️ UNRECONCILED` block — the agent
noticing that the person who signs is in the room for the first time, *and* that someone else in
that room told you something the wiki now knows was wrong. That's judgement, not summarization.
