# Use case: Account Researcher

**By 7:30 you'll have:** your own researcher skill, written with your agent, plus a real
Backgrounder on an account in your book, with an honest list of what is NOT known.

---

## Think first: where does account info live for you?

- Your CRM? Which one, and can you connect it yourself or does IT own it?
- An internal tool? Big companies often have an account-intel platform or an internal MCP.
  Ask whoever runs AI at your company what your agent is allowed to touch.
- The public web? Always available, zero setup: news, filings, job postings, leadership pages.

## Connect it: pick your lane

| Your situation | Do this tonight |
|---|---|
| Founder / self-admin | Connect your CRM's MCP (HubSpot, Attio) before you build |
| Corporate stack | Ask your agent to look for an internal MCP before assuming you have nothing. Otherwise web-only tonight; IT request Friday |
| Internal platform exists | Use it as a source you paste from tonight; wire it properly later |
| Nothing connected | Web search alone genuinely works. A scraper API (Firecrawl) adds depth later |

**How to connect it, the short version:**

- **Web only genuinely works tonight.** Zero setup: news, filings, job postings, leadership
  pages. Start here.
- **Your CRM, if you admin it:** Claude Desktop > Settings > Connectors > Add custom
  connector. Paste your CRM's MCP URL from its docs, sign in. Test: "list my accounts."
- **Corporate stack:** ask your agent whether an internal MCP or account-intel platform
  exists. Big companies often run them; Microsoft folks, ask Josefina.
- **Deeper scraping later:** a Firecrawl API key in `.env` (copy `.env.example` first).
  Keys live in `.env`, never in a wiki page.

Step-by-step recipes for every lane: [`../connect-guide.md`](../connect-guide.md)

## Build your version of the skill

The pro version ships in `automations/account-researcher.md`. **Don't open it yet.** Paste
this and let your agent teach you while you build:

> I want to build an account-researcher skill for my second brain. Interview me first, one
> question at a time: which account should we research, where does my account information
> live today (CRM? internal tools? only the web?), and what do I wish I always knew before a
> first call. If I have a source we can connect right now, walk me through connecting it;
> otherwise use web search. Then draft `automations/account-researcher.md` as a short prose
> playbook based on my answers, show it to me, and run it on my account. Cite every claim
> and keep facts separate from inferences.

## While it runs

- Facts and inferences must be labeled. "Hiring three Kafka engineers" is a fact; "building
  a streaming platform" is an inference.
- No invented numbers. Unknown means a gap on the list, not a guess.
- A "Gaps: needs confirmation" section is mandatory. A named gap is a to-do; a papered-over
  gap is a trap.

## Steal from the pro

Now open `automations/account-researcher.md` (the shipped one). Compare: did your version
think of job postings as a source? The fiscal-calendar question? Merge what yours is missing.

## Your 3-minute demo

Pick an account nobody in the room knows. Show the Gaps checklist and say why it is the most
useful section. Land the line: "this is all public information. The agent is not clairvoyant,
it is thorough, and thoroughness at this speed is the new part."
