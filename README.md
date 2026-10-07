<p align="center">
  <a href="https://xcut.ai/mcp"><img src="assets/banner.png" alt="XCut AI: ask your AI what's going viral" width="100%"></a>
</p>

<p align="center">
  <b>Find what's going viral on Instagram, TikTok, YouTube and Facebook, then write it in your brand's voice, right inside ChatGPT, Claude, Grok, Meta Muse, Gemini or your code editor.</b>
</p>

<p align="center">
  <a href="https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=XCut%20AI&connectorUrl=https%3A%2F%2Fmcp.xcut.ai%2Fmcp"><img alt="Add to Claude" src="https://img.shields.io/badge/Add_to-Claude-D97757?style=for-the-badge&labelColor=1a1a1a"></a>
  <a href="https://cursor.com/en/install-mcp?name=xcutai&config=eyJ1cmwiOiJodHRwczovL21jcC54Y3V0LmFpL21jcCJ9"><img alt="Add to Cursor" src="https://img.shields.io/badge/Add_to-Cursor-ffffff?style=for-the-badge&labelColor=1a1a1a"></a>
  <a href="https://vscode.dev/redirect/mcp/install?name=xcutai&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fmcp.xcut.ai%2Fmcp%22%7D"><img alt="Add to VS Code" src="https://img.shields.io/badge/Add_to-VS_Code-0098FF?style=for-the-badge&labelColor=1a1a1a"></a>
  <a href="https://xcut.ai/mcp"><img alt="All apps" src="https://img.shields.io/badge/Setup-All_apps-9F17AD?style=for-the-badge&labelColor=1a1a1a"></a>
</p>

<p align="center">
  <a href="https://xcut.ai">Website</a> ·
  <a href="https://xcut.ai/mcp">Setup guide</a> ·
  <a href="https://app.xcut.ai">Open XCut AI</a> ·
  <a href="https://xcut.ai/privacy-policy#ai-assistants">Privacy</a>
</p>

---

## Server URL

```
https://mcp.xcut.ai/mcp
```

Paste it into any app that supports remote MCP servers. Hooks, playbooks and quick tools work straight away with no account. Tools that use your canvases, brand memory or credits ask you to sign in to XCut AI once.

## What you can ask

> *"What's going viral on TikTok in the fitness niche this week?"*
>
> *"Which of @competitor's last 30 reels beat their normal views, and by how much?"*
>
> *"Get me the transcript of this reel, then write 3 versions for my brand."*
>
> *"Give me 10 hooks for a video about pricing mistakes."*
>
> *"Make a 2-week Instagram content plan from my research canvas and put it on my calendar."*
>
> *"What Meta ads are competitors running for protein powder?"*

## Install

<details open>
<summary><b>Claude</b> (web, desktop, mobile)</summary>

1. Click **Add to Claude** above, or open **Customize → Connectors → Add custom connector** and paste the server URL.
2. Under Authentication, choose **Sign in when needed**.
3. Ask anything. Claude asks you to sign in to XCut AI only when a tool needs your account.
</details>

<details>
<summary><b>ChatGPT</b> (also works in Dots)</summary>

1. Go to [chatgpt.com/plugins](https://chatgpt.com/plugins) and press **+** → **Add custom MCP server**.
2. Name it XCut AI, paste the server URL, choose **OAuth**, then **Create as a plugin**.

Write actions need a Business, Enterprise or Edu workspace. Pro can read.
</details>

<details>
<summary><b>Grok</b></summary>

Go to [grok.com/connectors](https://grok.com/connectors) → **New Connector → Custom**, paste the server URL and sign in.
</details>

<details>
<summary><b>Meta Muse</b></summary>

Create an API key in XCut AI under **Settings → Connected apps**, then ask Muse to create a custom connector for `https://mcp.xcut.ai/mcp` that sends it as `Authorization: Bearer <key>`.
</details>

<details>
<summary><b>Gemini</b></summary>

In Gemini on the web: **Settings → Connected Apps → Add a custom app**, paste the server URL and sign in.
</details>

<details>
<summary><b>Claude Code</b>: plugin with skills</summary>

```
/plugin marketplace add xcut-ai/xcutai-plugins
/plugin install xcutai@xcutai
```

Then run `/mcp` and sign in. Server only: `claude mcp add --transport http xcutai https://mcp.xcut.ai/mcp`
</details>

<details>
<summary><b>Codex</b>: plugin with skills</summary>

```
codex plugin marketplace add xcut-ai/xcutai-plugins
codex plugin add xcutai@xcutai
```

Server only: `codex mcp add xcutai --url https://mcp.xcut.ai/mcp`, then `codex mcp login xcutai`.
</details>

<details>
<summary><b>Cursor, VS Code, Perplexity, Le Chat and others</b></summary>

Use the buttons above, or add the server URL as a remote MCP server. Apps that can't sign in can use a personal API key from **Settings → Connected apps**:

```json
{ "mcpServers": { "xcutai": { "url": "https://mcp.xcut.ai/mcp", "headers": { "Authorization": "Bearer YOUR_XCUTAI_API_KEY" } } } }
```
</details>

## What's inside

| | Tools | Account |
|---|---|---|
| **Free** | Hook library (about 1,000 hooks from posts that performed), playbooks and platform facts, quick tools (captions, bios, titles, script scores, calendars, competitor gaps) | Not needed |
| **Discover** | Viral search across Instagram, TikTok, YouTube, Facebook and the Meta Ad Library · outliers scored against each account's own median · per-post analytics · breakouts in your watchlist | Sign in, uses credits |
| **Import** | Posts and videos (transcribed and broken down), whole profiles, websites, Meta ads | Sign in, uses credits |
| **Create** | Scripts, hooks, captions and ad copy from XCut AI's own agents, written with your brand memory · ready-made playbooks (month and week plans, teardowns, ad angles) | Sign in, uses credits |
| **Workspace** | Your canvases, brand memory, content calendar, credit balance | Sign in |

The plugin for Claude Code and Codex adds three skills that teach the assistant how to chain these tools: `viral-research`, `outlier-to-script` and `content-plan`.

## Good to know

- **Your data stays yours.** XCut AI never sees your chat history with the assistant. Usage records hold which tool ran and when, not what you asked, and are deleted after 90 days. [Privacy policy](https://xcut.ai/privacy-policy#ai-assistants).
- **You stay in control.** Disconnect any app or revoke any key in **Settings → Connected apps**, where you can also see every request it made.
- **It never posts for you.** XCut AI drafts and plans. It doesn't publish to social media.
- **Public data only.** XCut AI imports publicly available posts, profiles and ads, using official platform APIs and licensed data providers.

## Repository layout

```
.claude-plugin/marketplace.json    Claude Code marketplace
plugins/xcutai/                    Claude Code plugin: manifest, MCP config, skills
.agents/plugins/marketplace.json   Codex / ChatGPT marketplace
openai/xcutai/                     Codex / ChatGPT plugin: manifest, MCP config, skills
```

---

<p align="center">
  <a href="https://app.xcut.ai"><b>Try XCut AI free →</b></a><br>
  <sub>Questions: <a href="mailto:support@xcut.ai">support@xcut.ai</a></sub>
</p>
