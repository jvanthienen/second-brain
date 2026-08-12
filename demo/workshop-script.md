# Workshop script: the 10-minute demo

One arc, six beats, framed as a single Monday morning in Josefina's week: the news watch lands,
a meeting gets captured and ingested, the hood comes off, the QBR brief goes to the team.
Beat 5 was chosen from the registration data: pre-meeting prep got 7 of 12 votes and it
closes the story (the QBR is next Thursday). Top vote-getter pipeline review (8) lives in the
build-hour cards; it needs their CRM data, not your stage.

**Read [`story.md`](story.md) first.** Cast, timeline, tension. You are narrating Josefina's
week; the software plays itself.

---

## Screen setup

| Where | What |
|---|---|
| Left half | Claude Desktop, fresh chat, file access to the repo folder AND `~/Meetings`, Slack connected |
| Right half | Obsidian on the repo. Graph view in one tab, `wiki/log.md` in another |
| Behind | Slack, #nike-vteam channel visible |
| System | Notifications off (Focus mode). Font size up everywhere. |

---

## Pre-flight checklist

**On the Monday before (2 minutes, do not skip):**
- [ ] Post the staged news digest (text below) into #nike-vteam in the demo workspace, around
  8 AM. By Thursday it reads "Monday 8:02 AM" and nobody has to take your word for it.

**The day before:**
- [ ] Claude Desktop: file access to the repo folder AND `~/Meetings`. Test: "list the wiki
  pages", then "list my Meetings folder".
- [ ] Slack connector signed in, demo workspace, #nike-vteam exists. Never a real work channel.
- [ ] Stage the meeting file (run in the repo folder; sets the fiction to demo day):
  ```
  TODAY=$(date +%F)
  mv raw/_inbox/2026-08-07-nike-cfo-prebrief.md ~/Meetings/$TODAY-nike-qbr-prep-sofia.md
  sed -i '' "s/2026-08-07/$TODAY/g" ~/Meetings/$TODAY-nike-qbr-prep-sofia.md
  ```
  `raw/_inbox/` must be EMPTY (except its README). `~/Meetings` contains only the Sofia file.
- [ ] Dry run on a COPY, never the demo repo. Screen-record it: that recording is the backup.
- [ ] Claude Code open in a terminal as fallback surface.
- [ ] Obsidian graph view opens colored (accounts blue, people green, patterns orange,
  blockers red, motions purple).
- [ ] Read [`story.md`](story.md). Rehearse once, out loud, with a timer.

**The staged digest (post this Monday 8 AM, as yourself or a "News Watch" bot):**

> 📰 Account news, Monday
>
> 🔴 Nike: competitive
> Vertex Cloud announced enterprise price cuts for analytics workloads, effective Sept 1.
> They are already benchmarking us inside Nike finance. This lands a week before the QBR
> and makes any discount-led pitch weaker, not stronger. Term structure is now the only
> viable open.
> Source: vendor announcement · Confidence: high
>
> 🟡 Patagonia: hiring
> Two new ML-platform roles posted, both mention real-time inference. Supports the timing of
> Priya's inference proposal (review Aug 15).
>
> Nordstrom: nothing of note.

---

## Beat 1 (0:00-1:30): Monday, 8 AM. The news watch lands.

Open Slack, #nike-vteam. The digest is sitting there with Monday's timestamp. Read the 🔴
item aloud.

**Say:** "I did not search for this. An agent runs every Monday at 8, reads my whole book,
scans the news, and posts only what changes the plan. Most Mondays it posts nothing. This
Monday it changed the plan: the competitor cut prices a week before my most important
meeting of the quarter. The spec for this agent is one prose file in the repo."

---

## Beat 2 (1:30-2:30): capture, now

**Say first:** "An hour ago I finished my QBR prep call with Sofia Marchetti, my champion at
Nike. Her notes are in my meetings folder. Normally my 6 PM automation files the day's
meetings into the brain by itself. The QBR is next Thursday. I am not waiting for 6 PM."

Type in Claude Desktop:

> **Run my daily capture now (automations/daily-capture.md). I cannot wait for the 6 PM run.**

The Sofia file lands in `raw/_inbox/`, named and dated, with a one-line "1 source waiting"
digest.

**Say:** "Filing is the chore that kills every notes system. Mine does it at 6 PM every day
without me. I just needed it early."

---

## Beat 3 (2:30-6:00): the ingest (the bomb)

**First, show the note itself.** The captured file is now in `raw/_inbox/`, which is inside
the Obsidian vault: click it, scroll once, slowly.

**Say:** "This is just my meeting note. What she told me, section by section. My insights.
My next steps. No special format, no tags, no filing. Now watch where each piece GOES."

Type:

> **Ingest it. The QBR is next Thursday and I need to know what changed.**

While it works, narrate the routing. This is how you explain the wiki without ever defining
it: point at a section of the note, then at the page it landed on.

| Section of the note | Where it goes in the wiki |
|---|---|
| "On the cost review" | [[Nike]] account page, its ⚠️ Contradictions table, and [[Vertex Cloud]] |
| "On egress" | Second contradiction, and the [[Egress Cost Proposal]] motion gets downgraded |
| "What Rachel actually cares about" | [[Rachel Kim]] person page, and the [[Commitment Flexibility vs Discount Depth]] pattern |
| "On Daniel" | [[Daniel Osei]] person page, flagged as a new instance of [[Champion Dependency Risk]] |
| "Also" (marketplace) | The [[Nike Marketplace Listing Stalled]] blocker |
| "Insights" | Strengthen the pattern pages: inference becomes evidence |
| "Next steps" | The account page's open-threads table, with owners |

**Say:** "One note, seven destinations. That is the whole trick: the note stays raw forever,
and the STRUCTURE lives in the wiki. I never file anything. It knows where things go because
the schema file describes the page types."

What lands, in order of drama:

| It does | You say |
|---|---|
| Flags contradiction 1: the cost review was never routine, it is a competitive benchmark against [[Vertex Cloud]] running since May | "We were told in June it was routine. We believed that for two months. And it is the same competitor from this morning's news." |
| Flags contradiction 2: nobody in finance cares about egress | "We have been building the wrong proposal since June." |
| Rewrites [[Rachel Kim]]: first real intel on the economic buyer | "The person who signs. We knew almost nothing this morning." |
| Adds the [[Daniel Osei]] flight risk, a new instance of [[Champion Dependency Risk]] | "Our champion is interviewing elsewhere. The wiki connected that to a pattern it already knew." |
| Updates ~14 files, `index.md`, appends to `log.md` | Open the log tab. Show the new entry next to the previous six. |

**Say, landing it:** "One meeting. Twelve pages. And it just told me that two months of work
was aimed at an objection the buyer never had."

**On the log:** `wiki/log.md` is the brain's journal: one dated entry per ingest, appended
forever, saying what changed and why it mattered. In Obsidian it is just a file; open it in a
second tab before the demo (Cmd+click the filename opens a tab) and flip to it here. The
line: "Seven entries. Two months of working memory, written entirely by the agent."

**Dry-run notes (validated 2026-08-09, pre-retheme):**
- It creates NO new pages: every entity already has one. Narrate page CHANGES, not creation.
- It found a THIRD contradiction (Rachel was "hands-off" in June; she is actively
  benchmarking now). Bonus if it surfaces.
- Strongest framing: "the wiki was already suspicious. It had this marked as inference and
  the egress evidence marked thin. This meeting resolves both."

---

## Beat 4 (6:00-7:30): open the hood

Flip to Obsidian. Fast:

1. `raw/`: "Seven meeting records now. Immutable. The agent reads them, never edits them."
2. `wiki/`: "The agent wrote every page here. I have never edited one by hand."
3. `AGENTS.md`: "The whole configuration. It is prose."
4. Graph view: hover [[Commitment Flexibility vs Discount Depth]], connected to all three
   accounts.

**Say:** "This page is the reason the brain is not a chatbot. No single meeting contains it.
It emerged from three meetings, at three different accounts, weeks apart. And everything I
show you next is composed FROM these pages, not from a lucky prompt."

**Optional flourish if pacing allows (30 seconds):** type "Why do our commitment deals keep
stalling?" and let the cross-account answer land.

---

## Beat 5 (7:30-9:30): the QBR brief, to the whole team

Type:

> **Prep me for next Thursday's QBR with Rachel Kim, following automations/pre-meeting-prep.md. Save
> the brief as a file in briefs/ and post it to the #nike-vteam channel in Slack.**

The one-screen brief assembles from pages that changed five minutes ago. Look for:

| In the brief | Why it lands |
|---|---|
| 🔴 NEW next to Rachel Kim | The person who signs, in the room for the first time |
| ⚠️ UNRECONCILED: Tom's June "routine" framing vs Sofia's reality, and Tom is in the room | "Do not repeat the June framing back to anyone" |
| PATTERN IN PLAY: term structure, not price | This morning's news item just made this the only option |
| The objective: a relationship, not a close | Derived from open threads, not invented |

Review it on screen. **Discretion check:** the wiki now holds Daniel's off-the-record flight
risk, and this brief goes to a shared channel. Verify the draft leaves that detail out; if it
slipped in, delete the line on camera and say why. That edit is the gate doing its job, in
public.

Approve. Show both landings: the file in `briefs/` (Obsidian sidebar) and the post in
#nike-vteam, directly under Monday's news digest. The channel now tells the whole story.

**Say:** "A week before the meeting that decides a $12M renewal, my whole account
team has the same one-screen brief, assembled from everything the brain learned today.
Nothing auto-sent. I read it before it went anywhere."

---

## Beat 6 (9:30-10:00): the handoff

Face the room.

**Say:** "Everything you watched is three prose files and a folder of markdown. And when a
brand new account lands in my book, the same system researches it and builds the pages from
scratch. That is what you are about to do with your own accounts. Open WORKSHOP.md. Pick
your use case. Go."

---

## Contingencies

| If | Then |
|---|---|
| Capture step fumbles | Drag the file into `raw/_inbox/` in Finder yourself: "the 6 PM run does this unattended." Keep moving. |
| Ingest runs long | Keep narrating over Obsidian; the file changes are the show. At the 6-minute mark, cut to the log entry and the landing line. |
| Ingest goes sideways | Play the recording. Say so plainly: "this is this morning's run." |
| One file write spins for 2+ min | The writes often flush late: check Obsidian, the pages are usually already there. If truly stuck, press Stop and type "verify the ingest is complete; finish anything missing, then update index and log." It resumes, never restarts. |
| The agent asks a mid-ingest question (e.g. how to record the off-the-record intel) | Gift, not glitch. Read it aloud, pick the recommended option, say: "it asked before writing something sensitive. That is the schema working." |
| Claude Desktop chokes on multi-file edits | Fallback terminal with Claude Code, same prompts. |
| Slack connector fails | The brief on screen IS the demo. Paste it into the channel manually. |
| Running short | Cut the Beat 4 optional query. Shrink Beat 1 to 30 seconds. Never cut Beat 3 or Beat 5. |

## Audience questions

The crib is in [`runbook.md`](runbook.md), bottom section: RAG vs this, what stops it being
wrong, how long it took, connectors, what happens at 500 pages.

One more this demo invites, decide your stance beforehand:

**"You put off-the-record intel in a wiki?"**
The repo is private and local; access to the brain IS access to the intel, same as a notebook.
The schema records it marked confidential, and the shared brief left it out (or you removed it
on camera). The honest answer: the brain has the same discretion obligations you do, and the
nothing-auto-sends gate is where that discretion gets enforced.
