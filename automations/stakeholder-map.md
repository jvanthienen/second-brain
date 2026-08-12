# Agent — Stakeholder Map

**Trigger:** on demand — *"map the stakeholders at [company]"*
**Reads:** web + contact enrichment + your own network
**Writes:** `wiki/people/*.md`, the People section of the Account page, `index.md`, `log.md`
**Runtime:** 2–4 minutes

---

## What it does

Turns a company into a map of **who matters, who reports to whom, and where you have no
coverage.** The last part is the point.

Each person worth tracking gets a Person page. **The rule for who gets one: you'd write more
than a job title.** Everyone else lives in the Account page's People table.

---

## Process

### 1. Identify the roles that matter
Work backwards from the decision, not forwards from the org chart:

| Role | Why they matter |
|---|---|
| **Economic buyer** | Signs |
| **Technical decision maker** | Chooses |
| **Champion** | Advocates when you're not in the room |
| **Blocker** | Prefers an alternative |
| **User** | Lives with the outcome |

### 2. Populate from public sources
Professional networks, leadership pages, conference speakers, engineering blog authors, podcast
guests, open-source maintainers.

### 3. Enrich
Fill in titles and reporting lines. **Do not put personal contact details in the wiki** — see
Rules.

### 4. Find your paths
Cross-reference against your own network: shared connections, prior colleagues, alumni overlap.
**A warm path is worth more than a complete map.**

### 5. Score coverage
Per key role: **Strong** (regular contact) · **Weak** (met once) · **None**.

Then state the gap plainly. *"No relationship with the economic buyer, eight months from
signature"* is the most valuable sentence this agent produces.

### 6. Check for patterns
If an account is single-threaded with no executive coverage, that's an instance of
[[Champion Dependency Risk]] — update the Pattern page, don't just note it locally.

---

## Person page shape

```markdown
# Rachel Kim

> **Person page.** CFO, [[Nike]].
> **Last reviewed:** 2026-07-29 · **Sources:** 2 (both indirect)

## Who she is
## What we know          ← each claim with source + date
## What we don't know    ← explicit checklist
## Why she matters
## Related
```

---

## Rules

- **No personal contact details in the wiki.** Names, titles and reporting lines are fine.
  Direct numbers and personal emails are not — especially anything going on a screen.
- **Mark inferred reporting lines as inferred.** Public sources go stale.
- **Coverage is about you, not them.** "Strong" means you have the relationship.
- **Second-hand intel gets labelled second-hand.** A page built entirely on relayed claims
  should say so at the top.

---

## Demo notes

Best visual in the set after the graph — render coverage as colour, reporting lines as edges.

If you're showing a real company, keep contact columns off the screen. Names and titles are
public; someone's mobile number on a projector is a real privacy problem and the room notices.
