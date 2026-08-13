# AGENTS.md — the schema

> **This is the configuration file.** It's what makes the agent a disciplined wiki maintainer
> instead of a generic chatbot. Read it before touching anything in `wiki/`.
>
> Rename to `CLAUDE.md` for Claude Code, keep as `AGENTS.md` for Codex/Copilot CLI, or point
> your agent at it however it expects.

---

## The three layers

| Layer | Where | Who writes it | Rule |
|---|---|---|---|
| **Raw sources** | [`raw/`](raw/) | Nobody | **Immutable.** Read from, never modify. |
| **The wiki** | [`wiki/`](wiki/) | **The agent, entirely** | The human reads it. The agent writes it. |
| **The schema** | This file | Humans | Co-evolved as you learn what works. |

The wiki is not a filing cabinet for meeting notes. **It is a persistent, compounding synthesis
that sits between you and the raw sources.** When a new source arrives, you don't index it — you
read it, integrate it, and update everything it touches.

The knowledge is compiled once and kept current, not re-derived on every query.

---

## The rule that keeps it honest

Before writing any fact into a wiki page, ask:

> **Would I ever filter or compare every account by this?**

- **Yes** → it's structured data. It belongs in a table or the data layer. **Never restate it in prose.**
- **No** → it's prose, and it belongs in a wiki page.

Duplicating a fact in both places guarantees drift.

**Never put in a wiki page:** revenue figures, contract values, employee counts, agreement dates,
tech-stack lists, team rosters.

**Always put in a wiki page:** *why* something is happening, what it means, what contradicts
what, what's at risk, and how accounts connect to each other.

---

## Page types

| Type | What it is | Cadence | One per |
|---|---|---|---|
| **Account** | What's happening now — state of play, open threads, risks | Weekly | Account |
| **Backgrounder** | Who they are, market context, relationship history | Quarterly | Account |
| **Motion** | A commercial play running across accounts | As it moves | Play |
| **Pattern** | A behaviour or dynamic seen more than once | As observed | Pattern |
| **Blocker** | A specific thing that is stuck, with an owner | Until resolved | Instance |
| **Person** | A stakeholder worth tracking across meetings | As encountered | Person |
| **Company** | A third party that isn't an account — competitor, vendor | Rarely | Company |

### The three that get confused

|  | **Motion** | **Pattern** | **Blocker** |
|---|---|---|---|
| Who acts | We drive it | They do it, or it recurs | Someone owns unsticking it |
| Has | A playbook, stages, owners | Instances across accounts | An owner and a target date |
| Ends? | Yes — there's a finish line | No — it keeps showing up | Yes, then archive |
| Answers | *"Where are we on this?"* | *"Where else does this show up?"* | *"Who's fixing this, by when?"* |

A thing can be **both a Pattern and a Blocker**: the recurring dynamic gets a Pattern page, each
stuck instance gets its own Blocker page linking to it.

### Account vs Backgrounder

- **Account page** answers *"what's happening and what's at risk?"* — read before a meeting.
- **Backgrounder** answers *"who is this company?"* — read when you join the account.

If a fact will still be true in six months, it belongs in the Backgrounder.

---

## Page structure

Every page opens with a **context banner** pointing at its siblings:

```markdown
> **Living page — what's happening now.** For who they are, see [[Nike - Backgrounder]].
```

Then YAML-style frontmatter is optional but useful if you want Dataview-style queries later.

### Account page sections

1. **The one thing that matters** — the single fact everything else keys off
2. **Current state** — 2–3 paragraphs
3. **Themed sections** — commercial, technical, relationship; whatever the account needs
4. **People** — links to Person pages, with their role in this account
5. **⚠️ Contradictions** — where newer sources contradict older claims
6. **Open threads** — table: thread, owner, status
7. **Risks**

### Backgrounder sections

1. **The company** — what they do, origin, scale, funding
2. **Market context** — the market they compete in, where it's going
3. **Competitive position** — and what it means for us
4. **The relationship** — how it started, what happened, where it turned
5. **Gaps — needs confirmation** — an explicit checklist of what we don't know

### Motion / Pattern sections

1. **What this is** — one paragraph
2. **Where it shows up** — table of accounts and their position
3. **The insight** — the actual thing worth noticing, not a summary
4. **Open** — questions this raises

### Blocker sections

1. **What's blocked** — be specific about scope
2. **Why** — one paragraph, then link to the Pattern page if one exists
3. **Where it stands** — who's seen it, what's been proposed
4. **Owners** — named, both sides
5. **What has not been tried** — the most useful section; stops the team re-deriving
6. **Impact if unresolved** — honestly
7. **Next step** — one action

---

## Contradictions are first-class

**When a new source contradicts an existing page, never silently overwrite.**

Add or update a `## ⚠️ Contradictions` section:

```markdown
## ⚠️ Contradictions

| Old claim (dated) | Reality (dated) | Which matters |
|---|---|---|
| Cost review is routine and internal (2026-06-02, procurement) | It's a competitive benchmark against [[TWS]] (2026-08-07, VP Eng) | The new one. It reframes the renewal from a paperwork exercise into a defence. |
```

Then say which one matters and why.

**A claim that quietly changed is more dangerous than one never written down.** The contradiction
section is often the most valuable thing on the page — it's the record of what you used to
believe and why you stopped.

---

## Cross-links

Use `[[Page Title]]` inline, matching the page title exactly. Obsidian resolves these regardless
of folder.

Link generously. **A page with no inbound links is an orphan** — surface it in the next lint pass.

---

## The three workflows

### 1. Ingest

A new source lands in [`raw/_inbox/`](raw/_inbox/). Then:

1. **Read it fully.** Don't skim for entities.
2. **Discuss the key takeaways with the human** before writing. They may know context the source
   doesn't carry.
3. **Update every page it touches.** A meaningful source touches **8–15 pages.** If you only
   touched two, you under-processed it.
4. **Create new pages** when the source introduces a genuinely new person, motion, pattern or
   company. Don't force new material into existing pages.
5. **Flag contradictions explicitly** — see above. This is the highest-value step.
6. **Update [`wiki/index.md`](wiki/index.md)** with any new pages.
7. **Append to [`wiki/log.md`](wiki/log.md)**.
8. **Move the source** from `_inbox/` to `raw/transcripts/` or `raw/notes/`.

> **The test of a good ingest:** it changes what you'd *do*, not just what you'd *know*.

### 2. Query

1. **Read [`wiki/index.md`](wiki/index.md) first** to find relevant pages, then drill in.
2. Answer with **citations to page titles**.
3. Prefer synthesis across pages over quoting one page. If the answer sits entirely in one page,
   the question was probably too narrow.
4. **File good answers back into the wiki as new pages** — usually a Motion or a Pattern.

> **Explorations should compound, not vanish into chat history.**

### 3. Lint

Periodically, health-check the wiki:

- Pages not reviewed in 30+ days
- Contradictions recorded but never reconciled
- **Orphans** — pages with no inbound links
- Concepts mentioned across several pages with no page of their own
- Gaps checklists on Backgrounders that could now be closed
- Stale claims a newer source has superseded

Report findings. Don't silently fix — some "orphans" are deliberate.

---

## Honesty rules

These matter more than anything else here.

- **Never invent a number.** If you didn't pull it, write `—` and say where it would come from.
- **Never write `$0` as a placeholder.** A zero claims the account has no revenue; a dash admits
  you don't know. Confusing these will eventually put a false statement in front of a customer.
- **Every claim carries a source and a date.** `(2026-08-07, Sofia Marchetti pre-brief)`.
- **Distinguish fact from inference.** Label inferences as inferences.
- **Say what you couldn't find.** A named gap is useful; a papered-over gap is a trap.
- **"I don't know" is a complete answer.** Follow it with how you'd find out.

---

## Operating rules

- **Nothing auto-sends.** Draft → human reviews → it goes. Email, chat, CRM, everything.
- **The human owns sourcing and questions. The agent owns bookkeeping.** Summarizing,
  cross-referencing, filing, and consistency — that's the agent's job, and it's the job humans
  abandon wikis over.
- **Read [`docs/soul.md`](docs/soul.md) before producing any written artifact**, then the
  matching format spec in [`playbooks/`](playbooks/).
- **Default to the short version.**

---

## Where things live

| Need | Location |
|---|---|
| Who the human is, what they own | [`BRAIN.md`](BRAIN.md) |
| What's happening at an account | `wiki/accounts/<slug>.md` |
| Who a company *is* | `wiki/backgrounders/<slug>.md` |
| Cross-account plays and dynamics | `wiki/motions/`, `wiki/patterns/` |
| What's stuck | `wiki/blockers/` |
| Catalog of every page | [`wiki/index.md`](wiki/index.md) |
| What happened when | [`wiki/log.md`](wiki/log.md) |
| Source documents | [`raw/`](raw/) — immutable |
| How to write something | [`docs/soul.md`](docs/soul.md) + [`playbooks/`](playbooks/) |
| What an agent does | [`automations/`](automations/) |
