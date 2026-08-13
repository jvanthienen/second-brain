# Workshop script: the 5-minute demo

One story, one character, one use case. The room meets Daniel in the slides, the demo shows
the brain catching something about him, and the payoff is the QBR brief that tells you how
to run the room because of it. Everything else the brain did stays on screen but un-narrated.

Rewritten 2026-08-12 from the co-host review: introduce Daniel at the very start and
reinforce him on every slide; keep the demo to a single story and use case; do not layer
insights; have a plan B; simplify the Obsidian view.

**Read [`story.md`](story.md) first.** Cast, timeline, tension. You are narrating one week
of Josefina's life; the software plays itself.

**Depends on the slides:** by the time the demo starts, the audience already knows Daniel
Osei (Nike, Head of Data Platform, your technical champion) from the deck. The demo never
introduces him, it pays him off.

---

## The story in one breath

You met Daniel in the slides. An hour ago your champion Sofia told you, off the record, that
Daniel is interviewing elsewhere. Her meeting note goes into the brain, the brain rewrites
Daniel's page, ties him to a pattern it already knew, and a week before the QBR your team
gets two things because of it: the brief that says how to handle the room, and the one-page
backgrounder everyone walks in holding. One meeting in, one decision out.

---

## Screen setup

| Where | What |
|---|---|
| Left half | Claude Desktop, fresh chat, file access to the repo folder, Slack connected |
| Right half | Obsidian on the repo. ONE tab open: the Sofia note in `raw/_inbox/`. Both sidebars closed. |
| Behind | Slack, #nike-vteam channel visible |
| System | Notifications off (Focus mode). Font size up everywhere. |

The old Monday news digest already sits in #nike-vteam with a real Monday timestamp. Leave
it: it is set dressing now, not a beat. If someone notices it, that is a bonus question.

---

## Pre-flight checklist (the day before)

- [ ] Claude Desktop: file access to the repo folder. Test: "list the wiki pages".
- [ ] Slack connector signed in, demo workspace, #nike-vteam exists. Never a real work channel.
- [ ] Stage the meeting file with today's date, directly in the inbox (run in the repo folder):
  ```
  TODAY=$(date +%F)
  mv raw/_inbox/2026-08-07-nike-cfo-prebrief.md raw/_inbox/$TODAY-nike-qbr-prep-sofia.md
  sed -i '' "s/2026-08-07/$TODAY/g" raw/_inbox/$TODAY-nike-qbr-prep-sofia.md
  ```
  `raw/_inbox/` contains ONLY this file (plus its README). Nothing goes in `~/Meetings`.
- [ ] Obsidian, simplify hard (this was direct feedback: too much on screen):
  - Close the left sidebar and the right sidebar.
  - One tab open: the staged Sofia note.
  - After the dry run, practice opening the LOCAL graph on [[Daniel Osei]] (open the page,
    then run "Open local graph", set depth to 1). You show Daniel's corner of the brain,
    never the full galaxy. The full graph is a slide, not a demo prop.
- [ ] Dry run on a COPY, never the demo repo. Screen-record the whole run: that recording is
  Plan B. Note which files changed so you can narrate from knowledge, not hope. Keep the
  dry run's backgrounder PDF on the Desktop: it is the backup attachment.
- [ ] Practice Obsidian's **Export to PDF** once on any wiki page (command palette, "Export
  to PDF"). Beat 4 uses it live.
- [ ] Claude Code open in a terminal behind everything, same folder, as fallback surface.
- [ ] Rehearse once, out loud, with a timer. Target 5:30, hard stop 6:00.

---

## Beat 1 (0:00-0:45): the note

Obsidian is already showing the Sofia note. Scroll it once, slowly. Stop at the "On Daniel"
section and read the key line aloud.

**Say:** "You met Daniel in the slides: my technical champion at Nike, the one who runs the
platform my renewal depends on. An hour ago I finished my QBR prep call with Sofia, my
champion. This is just my meeting note: what she told me, my insights, my next steps. No
tags, no filing, no format. My capture automation normally files the day's meetings at 6 PM;
today I ran it early, so the note is already sitting in the brain's inbox. Buried in the
middle, one sentence, off the record: Daniel is interviewing elsewhere."

---

## Beat 2 (0:45-3:15): the ingest, and the three things I had wrong

Type in Claude Desktop:

> **Ingest the note in raw/_inbox. The QBR with Rachel Kim is next Thursday. When you
> finish, give me the main insights from this call: the things I had wrong before it,
> numbered.**

When the numbered recap appears, read it off the screen. Expect the shape (wording will
vary; read what it wrote):

1. The "routine" cost review is a live benchmark against TWS, running since May.
2. The egress proposal answers an objection nobody in finance actually has.
3. Daniel is interviewing elsewhere.

**Say:** "That is what one meeting note changed. Two strategy corrections and one human
being. Numbers one and two stay in the wiki; your kit walks them. Number three is the story
tonight."

From here, stay on Daniel. Do not tour the other changes. The discipline of this beat:
one character, one thread, even while twelve files update around it.

| It does | You say |
|---|---|
| Rewrites [[Daniel Osei]]: the flight risk lands on his page, marked off the record | "One sentence in a prep call just became durable memory. Next month I will not remember Sofia said this. The brain will." |
| Links him to [[Champion Dependency Risk]], a pattern page that already existed | "It did not just file the fact. It recognized the fact as an instance of a risk it already knew about: too much of this account runs through one person." |
| Infers his working style from months of meeting notes: evidence over enthusiasm | "Nobody typed that. It read every meeting Daniel appears in and worked out how he decides. When I sit with him next, I bring benchmarks, not vision decks." |

(The working-style inference appeared in the 2026-08-11 rehearsal run. If this run words it
differently, read what it wrote; if it skips it, the flight risk plus the pattern link carry
the beat alone. Never promise the room a specific sentence.)

**Land the beat:** "One meeting note. The brain updated a dozen pages, but the story is:
it heard one off-the-record sentence about one person and turned it into memory, risk, and
a playbook for how to work with him."

---

## Beat 3 (3:15-4:00): Daniel's corner of the brain

Flip to Obsidian. Open [[Daniel Osei]], then the local graph (depth 1). A handful of nodes:
Daniel, Nike, Sofia, the pattern page.

**Say:** "This is Daniel's corner of my brain. His page: written by the agent, never by me.
The links: to the account, to the people around him, to the risk pattern. Every page you
saw update lives in a folder of markdown files on my laptop. That is the whole trick."

Do NOT open the full graph view. Do not open the log. One page, one local graph, out.

---

## Beat 4 (4:00-5:30): the payoff, brief plus backgrounder

Type:

> **Prep me for next Thursday's QBR with Rachel Kim, following
> automations/pre-meeting-prep.md. Two artifacts: the team brief, and the one-page
> backgrounder (who is in the room, goals, key points, what we just learned). Save the
> backgrounder in briefs/, then post the brief to the #nike-vteam channel in Slack.**

Both assemble from pages that changed three minutes ago. Narrate ONLY the Daniel lines
while it drafts:

| In the output | Why it lands |
|---|---|
| Brief: Daniel, bring evidence, not enthusiasm | The working style, now operational advice for the room |
| Brief: continuity risk flagged for the account | The off-the-record intel, translated into something a team can act on |
| Backgrounder: who is in the room, goals, key points, what we just learned (numbered) | The one-pager the whole team walks in holding |

**Discretion check, on camera:** both artifacts travel, and the wiki holds Daniel's flight
risk off the record. Verify BOTH keep the raw detail out (expect a neutral line like
"single-threaded risk on the technical side"). If it slipped in, delete the line in front
of everyone and say why: "nothing auto-sends; this gate is where discretion lives."

Approve. The brief posts to #nike-vteam. Then the attachment, by hand and on camera:

1. The backgrounder is now in `briefs/` (it appears in Obsidian).
2. Open it, run Obsidian's **Export to PDF** (practiced in pre-flight).
3. Drag the PDF into the #nike-vteam message thread.

**Say while dragging:** "The brief is the corridor read. The PDF is the one-pager everyone
walks into the room holding: who is there, the goals, and what we just learned, numbered.
I attach it myself, because nothing leaves this laptop without my hands on it."

**Say, and this is the handoff:** "One meeting went in. A week before the meeting that
decides a $12M renewal, my whole team knows how to handle the room, and the one thing that
should stay private stayed private. That loop, note in, judgment out, is what you build for
your own accounts right now. Open WORKSHOP.md. Pick your use case. Go."

---

## Plan B (decided in advance, not improvised)

**The recording is the parachute.** The pre-flight dry run is screen-recorded end to end.
If the live ingest breaks in any way you cannot talk over, say it plainly: "this is this
morning's run", play the recording from Beat 2, and keep narrating the same lines. The
demo is the narration, not the liveness.

| If | Then |
|---|---|
| Ingest runs long | Keep narrating Daniel over Obsidian; the file changes are the show. At 3:00, flip to [[Daniel Osei]] even if writes are still flushing; the page is usually already there. |
| One file write spins for 2+ min | Press Stop, type "verify the ingest is complete; finish anything missing, then update index and log." It resumes, never restarts. |
| The agent asks a mid-ingest question (e.g. how to record off-the-record intel) | Gift, not glitch. Read it aloud, pick the recommended option: "it asked before writing something sensitive. That is the schema working." |
| Ingest goes sideways entirely | Play the recording. |
| Claude Desktop chokes | Fallback terminal with Claude Code, same prompts, same folder. |
| Slack connector fails | The brief on screen IS the demo. Paste it into the channel by hand. |
| PDF export fumbles | Drag the backgrounder .md into Slack instead (it renders fine), or drag the dry-run PDF from the Desktop. |
| Running long at 4:00 | Skip the local graph (Beat 3). Never skip the discretion check. |
| Running long at 5:00 | Post the brief, drag the dry-run PDF, land the handoff line. |

---

## Cut beats (in your pocket, not in the demo)

These were in the 10-minute version. They are good material for Q&A or a second wind, and
they are all still in the kit; they are just not part of Daniel's story tonight.

- **The Monday news watch.** The digest still sits in #nike-vteam. If someone asks about it:
  "an agent reads my whole book every Monday at 8 and posts only what changes the plan."
- **The live capture run.** `automations/daily-capture.md` files the day's meetings at 6 PM.
  Tonight it happened off screen.
- **The cross-account pattern query.** "Why do our commitment deals keep stalling?" is the
  single best question if someone asks what makes this different from a chatbot: the answer
  spans three accounts and exists in no single meeting.
- **The full routing map.** One note feeds seven kinds of pages (account, people, patterns,
  blockers, motions, open threads, log). The kit's WORKSHOP.md walks it.

## Audience questions

The crib is in [`runbook.md`](runbook.md), bottom section: RAG vs this, what stops it being
wrong, how long it took, connectors, what happens at 500 pages.

One more this demo invites, decide your stance beforehand:

**"You put off-the-record intel in a wiki?"**
The repo is private and local; access to the brain IS access to the intel, same as a
notebook. The schema records it marked confidential, and the shared brief left it out (or
you removed it on camera). The honest answer: the brain has the same discretion obligations
you do, and the nothing-auto-sends gate is where that discretion gets enforced.
