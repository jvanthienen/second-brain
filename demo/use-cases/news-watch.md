# Use case: News Watch

**By 7:30 you'll have:** your own news-watch skill with YOUR definition of "material," and a
filtered digest for your real accounts where every item says what it means for your plan.

---

## Think first: what news actually changes your plan?

- Funding, M&A, exec moves, layoffs, public cost complaints: almost always material.
- Product launches, awards, conference slots: almost never.
- Where does news about YOUR accounts actually appear? Industry press? Their careers page?
  Their competitors' announcements?
- Where would you want the digest delivered: chat, a channel your team reads, email?

## Connect it: pick your lane

| Your situation | Do this tonight |
|---|---|
| Everyone | Nothing to connect. Web search is built into your agent |
| Want it delivered to the team | Slack or Teams connector, one click, later |
| Want it every Monday 8 AM | Scheduling is a take-home: one cron line, in the pro skill file |

**How to connect it:**

1. Nothing to connect: web search is built into your agent. Start building.
2. Give your filter a trusted-sources starting list and let it grow per account: Reuters,
   Bloomberg, Wall Street Journal, New York Times on the business wires; The Information
   and TechCrunch for tech; Yahoo Finance and SEC filings for public companies; the
   account's own newsroom and careers pages. Anything that only shows up off-list gets
   flagged as unverified, not dropped silently.
3. Optional, delivery to a channel: Claude Desktop > **Settings > Connectors** > Slack >
   **Connect**, approve in the browser.
4. Optional, every Monday 8 AM: the cron line ships in the pro skill file.

Step-by-step recipe for every connection: [buildergeneralist.com/second-brain](https://www.buildergeneralist.com/second-brain)

## Build your version of the skill

The pro version ships in `automations/news-watch.md`. **Don't open it yet.** Paste this:

> I want to build a news-watch skill for my second brain. Interview me first, one question
> at a time: which accounts and competitors should it watch, what kinds of news would
> actually change what I do in a week, and what should it NEVER bother me with. Then draft
> `automations/news-watch.md` as a short prose playbook with my include/skip filter, show
> me, and run it for the last 14 days. For each item, connect it to what the wiki knows and
> say what it means for my position. If nothing passes my filter, tell me nothing passed,
> and why that is the correct output.

## While it runs

- The filter is the product. Anyone can pipe headlines into a channel.
- Every item links its source.
- Anything contradicting a wiki page gets flagged loudly.

## Steal from the pro

Open `automations/news-watch.md` (shipped). Compare filters: did yours include "anything
contradicting a wiki page"? The "silence is a valid output" rule? Merge.

## Your 3-minute demo

Show one item where the agent connected news to your plan ("this makes X urgent because...")
rather than relaying a headline. If it found nothing material, demo exactly that: an
assistant confident enough to send nothing is the boldest claim in the room.
