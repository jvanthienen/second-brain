# Connect guide: every recipe, step by step

The use-case cards tell you WHICH connection you need. This page shows you HOW, click by
click. Nothing here is required to start: the brain works with zero connections.

---

## Recipe 0 · Install the brain into your agent

This is the one everyone does. "Installing" just means giving your AI access to the folder.

**Claude Desktop (recommended)**
1. Open a new chat.
2. Type: "Open the folder second-brain in my Documents and read AGENTS.md and BRAIN.md."
3. A permission box appears: "Claude would like to add this folder." Click **Add folder**.
4. Sanity check: ask "list the wiki pages." If it lists accounts and people, you are live.

**Claude Code (terminal)**
1. `cd ~/Documents/second-brain`
2. Rename `AGENTS.md` to `CLAUDE.md` (Claude Code's config name), then run `claude`.
3. Same sanity check: "list the wiki pages."

**Codex (ChatGPT desktop) / Copilot CLI / Gemini CLI**
1. Point the workspace at the folder (Codex) or run the CLI inside it.
2. These tools read `AGENTS.md` natively. Sanity check as above.

**First real sentence to say after install:**
> Read AGENTS.md and BRAIN.md. Then interview me and rewrite BRAIN.md so it is about me, not
> the sample persona.

---

## Recipe 1 · A connector (Slack, Gmail, Calendar) in Claude Desktop

The one-click lane. Used by: Exec & Team Update, Pre-Meeting Prep (calendar), News Watch
delivery.

1. Claude Desktop > **Settings > Connectors**.
2. Find Slack (or Google Calendar, Gmail) > **Connect**.
3. Your browser opens: sign in to YOUR workspace and approve.
4. Back in the chat, test it: "post 'test' to my own DM in Slack." Delete the test after.

Corporate warning: if sign-in dies on a company SSO screen, that is your IT approval
process talking. Use the fallback tonight; send the request Friday.

---

## Recipe 2 · A custom MCP server (your CRM and most modern tools)

The power lane. Used by: Pipeline Review (HubSpot, Attio), Account Researcher, Pre-Meeting
Prep (Granola, WorkIQ), Stakeholder Map (Happenstance), and more every month.

1. Find the server: search "<your tool> MCP server" in the tool's docs. If it exists, it is
   a URL (and sometimes an API key).
2. Claude Desktop > **Settings > Connectors > Add custom connector**.
3. Paste the URL, sign in when the browser opens.
4. Test: "using the <tool> connection, list my open deals."

Known-good MCPs tonight: HubSpot, Attio, Granola (`https://mcp.granola.ai/mcp`), WorkIQ
(Teams), Happenstance.

**On Microsoft Copilot:** MCP servers connect through your company's Copilot setup, not a
personal settings screen. Ask your agent what is already wired: big companies often run
internal MCPs (Microsoft does; ask Josefina at the workshop).

If the tool has no MCP yet, it almost certainly has an API or an export button. Recipes 3
and 4 cover you.

---

## Recipe 3 · An API key (Firecrawl, Happenstance, Fireflies)

The keys lane. Used by: Account Researcher (scraping), Stakeholder Map (Happenstance),
Pre-Meeting Prep (Fireflies/Otter).

1. Create the account, find "API keys" in its settings, copy the key.
2. In the brain folder, copy `.env.example` to `.env` and paste the key there. The `.env`
   file is gitignored: keys never end up in your wiki or your git history.
3. Tell your agent: "My Firecrawl key is in .env. Use their API when you research."

Rule: keys live in `.env`, never in a wiki page, never in a chat you might share.

---

## Recipe 4 · Your meeting notes (Granola, Teams, Otter)

The fuel lane. Used by: everything. This is Step 2 of WORKSHOP.md.

- **Granola**: connect the official Granola MCP (Recipe 2, URL `https://mcp.granola.ai/mcp`)
  and your meetings flow in. Newer Granola versions encrypt the local cache, so the MCP is
  the reliable lane; copying a transcript out of the app into `raw/_inbox/` always works.
- **Teams**: connect the WorkIQ MCP (Recipe 2) so your meeting history is queryable.
  Fallback: open a meeting recap, copy the transcript, paste into a file in `raw/_inbox/`.
- **Otter / Fireflies**: export the transcript (or connect their API, Recipe 3).
- **No notetaker**: type what you remember from a real meeting into a file. Memory counts.

---

## Recipe 5 · Your LinkedIn network

Used by: Stakeholder Map.

1. LinkedIn > Settings > **Data privacy** > "Get a copy of your data".
2. Tick **Connections** only. Request. The CSV arrives by email in about 10 minutes.
3. Drop `Connections.csv` into `data-pipeline/`.
4. Tell your agent: "My LinkedIn connections are in data-pipeline/. Cross-reference warm
   paths when you map stakeholders."

---

## The rule that makes all of this safe

Whatever you connect, the gate stays the same: **agents draft, you review, then it goes.**
No connection ever gets permission to act without you.
