# Agent: Daily Capture

**Trigger:** scheduled, weekdays 6:00 PM
**Reads:** your capture folder (wherever meeting notes and transcripts land on your machine)
**Writes:** `raw/_inbox/`, plus a one-line digest to you
**Runtime:** under a minute

---

## What it does

Sweeps your capture folder every evening and files anything new into `raw/_inbox/`, named and
dated, then tells you what is waiting. **It never ingests unattended.** You come back to a
stocked inbox, say "ingest", and the brain absorbs your day.

This is the automation that makes the brain compound without willpower. Wikis die because
filing is a chore humans abandon. This removes the chore and keeps the human on the one step
that needs judgment.

---

## Setup

Pick the folder where your meetings already end up: your notetaker's export directory, a
Downloads subfolder, a "Meeting Notes" folder you drag files into. One folder, written down:

| Setting | Value |
|---|---|
| Capture folder | `~/Meetings` (change to yours) |
| Schedule | Weekdays 6:00 PM local |
| Destination | `raw/_inbox/` |

---

## Process

1. **List the capture folder.** Anything new since the last run (new file, or modified today).
2. **Skip what is already filed.** A file whose content is already in `raw/` gets skipped, not
   duplicated.
3. **Normalize the name:** `YYYY-MM-DD-<account>-<topic>.md`. Date from the meeting, account
   inferred from attendees or title. If unsure, keep the original name and say so.
4. **Copy into `raw/_inbox/`.** Copy, never move or edit. Immutability starts at capture.
5. **Digest, one line:** "2 sources waiting in _inbox: nike-pricing-sync, patagonia-standup.
   Say ingest when ready." Nothing new means **no message at all.**

---

## Scheduling it

The spec above is prose; any scheduler that can invoke your agent works.

**Claude Code (simplest):** ask it, in the repo folder:

> Schedule this for me: every weekday at 6 PM, run automations/daily-capture.md against
> ~/Meetings.

It will set up the recurring run (cron under the hood) and confirm the schedule. To see it:
`crontab -l`. Equivalent cron line, if you prefer writing it yourself:

```
0 18 * * 1-5  cd ~/second-brain && claude -p "Run automations/daily-capture.md"
```

**Other tools:** any scheduled-agent feature pointing at this file does the same job. The
automation is the prose, not the plumbing.

---

## Rules

- **Never ingest unattended.** Filing is automatic; integration waits for a human. Same rule
  as [News Watch](news-watch.md).
- **Copy, never edit.** The source lands byte-identical. `raw/` immutability starts here.
- **Silence is a valid output.** Empty folder, no message.
- **When account attribution is unsure, say so** rather than guessing a name.

---

## Demo notes

This is the automation to build LIVE in front of a room. It is one sentence, it schedules in
seconds, and it lands the biggest idea in the system: the brain feeds itself every evening,
and you stay the editor.

Stage a fake transcript in the capture folder beforehand, then after scheduling, say "run it
once now" and watch it file today's meeting into the inbox on screen.
