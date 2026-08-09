# Agent — Account Researcher

**Trigger:** on demand — *"research [company]"*
**Reads:** web only
**Writes:** `wiki/backgrounders/<slug>.md`, `wiki/accounts/<slug>.md`, `index.md`, `log.md`
**Runtime:** 3–6 minutes

---

## What it does

Takes a company name and produces a **Backgrounder** and a stub **Account page** from public
sources. Works on a cold account — one you know nothing about.

Build this first. It needs no CRM, no calendar, no internal data.

---

## Process

### 1. Establish the basics
Website, size, funding, ownership, headquarters, recent leadership changes. For public
companies, the latest filings. Note the fiscal calendar — it drives their buying cycle and
it's the thing most people get wrong.

### 2. Understand the business
- What do they sell, and who actually buys it?
- Where are the margins?
- Who are their three main competitors?
- What did leadership say publicly in the last two quarters?

### 3. Map the technology
**Job postings are the highest-signal public source and are consistently underused.** A team
hiring for a specific database is already running it. Also: engineering blog, conference talks,
open-source contributions, status page.

### 4. Find the commercial angle
Where does spend concentrate? What are they publicly complaining about? Any event that forces a
decision — funding, acquisition, outage, regulation, public offering?

### 5. Write the pages

**Backgrounder** gets everything durable — company, market, competitive position, relationship
history, and an explicit **Gaps — needs confirmation** checklist.

**Account page** gets a stub: what's happening now is mostly unknown for a cold account, and
saying so is more useful than inventing it.

### 6. Register and log
Update `wiki/index.md`. Append to `wiki/log.md`.

---

## Rules

- **Cite every non-obvious claim** inline.
- **Distinguish fact from inference.** "Hiring three Kafka engineers" is a fact. "Building a
  streaming platform" is an inference. Label it.
- **Never invent a number.** No revenue estimate, no headcount guess.
- **The Gaps checklist is mandatory.** A named gap is useful; a papered-over gap is a trap.
- **Don't create Person pages here** — that's [Stakeholder Map](stakeholder-map.md)'s job.

---

## Demo notes

Pick a company **nobody in the room has context on**. Watching a brief get built from nothing is
far more convincing than revealing one you already had.

Say the quiet part: this is public information, assembled fast. The agent isn't clairvoyant,
it's *thorough* — and thoroughness at this speed is what's actually new.
