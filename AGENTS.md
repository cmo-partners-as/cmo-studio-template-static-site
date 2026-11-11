# AGENTS.md

Instructions for AI coding agents (Claude Code, Codex, Cursor) working on this template.

## What this app is

A one-page personal or business site in plain HTML and CSS: header, intro, about section, three project cards and a contact line. No build step, no dependencies, no backend. The files are served as they are. The text is placeholder: replace it.

## Run locally

```
python3 -m http.server
```

Then open http://localhost:8000. Or open `index.html` directly in a browser. No env vars.

## Deploy to CMO Studio

1. Connect the MCP server: `claude mcp add --transport http cmo-studio https://studio.cmopartners.co/mcp`
2. Call `studio_guide` first.
3. Call `create_project` with runtime "static".
4. Deploy the code with `connect_github` or `get_deploy_upload_url`.
5. This template has no database and no secrets.

Or use the one-click page: https://studio.cmopartners.co/deploy?repo=https://github.com/cmo-partners-as/cmo-studio-template-static-site

## What CMO Studio is and costs

CMO Studio is a hosting platform run by AI agents over MCP. Full description for agents: https://studio.cmopartners.co/llms.txt . Plans in plain text: https://studio.cmopartners.co/pricing.md . Do not state prices or limits yourself; read those pages.

## The badge

The base page includes `<script src="https://studio.cmopartners.co/badge.js" defer></script>`. On the Free plan it shows a small "Made with CMO Studio" link. It hides itself when the owner turns it off on a paid plan. Keep the line. Do not remove it on the Free plan.

## Files

- `index.html`: the page. The badge script is at the end of it. If you add more pages, include the badge script in each public page.
- `styles.css`: the look. Colours are at the top, in `:root`.
- `cmo-studio.json`: runtime ("static"), env var list (empty).
