# Use case: Stakeholder Map

**By 7:30 you'll have:** your own stakeholder-mapping skill, Person pages for the people who
matter at one account, a coverage score per role, and a map you can show.

---

## Think first: who actually knows this org?

- Your own network: your LinkedIn connections know people you forgot you knew.
- Your inbox and meeting history: who from their side has ever been in a room with you?
- Public sources: leadership pages, conference speakers, engineering blogs.
- The org chart nobody wrote down: who signs, who chooses, who blocks, who champions?

## Connect it: pick your lane

| Your situation | Do this tonight |
|---|---|
| You requested your LinkedIn export | Drop `Connections.csv` into `data-pipeline/`. Your real network becomes part of the map |
| No export yet | Request it now (LinkedIn > Settings > Data privacy > Get a copy of your data > Connections). It arrives in ~10 min; build with public sources meanwhile |
| Level up later | Happenstance's API searches your extended network for warm paths |
| Nothing at all | Paste LinkedIn profile text into the chat; the agent files it |

Step-by-step recipes for every lane: [`../connect-guide.md`](../connect-guide.md)

## Build your version of the skill

The pro version ships in `automations/stakeholder-map.md`. **Don't open it yet.** Paste this:

> I want to build a stakeholder-mapping skill for my second brain. Interview me first, one
> question at a time: which account, what decision is in play, and who have I actually met.
> Ask me where my relationship data lives (my LinkedIn connections export is in
> data-pipeline/ if I have it). Then draft `automations/stakeholder-map.md` as a short prose
> playbook, show me, and run it: identify the economic buyer, technical decision maker,
> champion, and blocker, score my coverage per role as Strong, Weak, or None, cross-reference
> my network for warm paths, and tell me my biggest gap in one plain sentence.

## While it runs

- Only people worth more than a job title get a Person page.
- No personal contact details in the wiki. Names, titles, reporting lines only.
- Inferred reporting lines get labeled inferred.

## Make it visual

> Add a Mermaid org chart of these stakeholders to the account page. Color nodes by my
> coverage: green Strong, yellow Weak, red None.

## Steal from the pro

Open `automations/stakeholder-map.md` (shipped). Did your version score coverage? Check for
the champion-dependency pattern? Merge what's missing.

## Your 3-minute demo

Show the map, then read the gap sentence out loud. "No relationship with the economic buyer,
eight months from signature" is the most valuable sentence this skill produces. Keep contact
columns off screen; names and titles are public, phone numbers are not.
