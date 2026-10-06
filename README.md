# Investor Search

Build a sourced list of the investors in a market — family offices, VCs, PE firms and
angels — and say honestly how complete it is.

By **BCP partners GmbH** · [bcpp.io](https://www.bcpp.io)

## Install

**Gemini CLI** — as an extension:

```
gemini extensions install https://github.com/verun-ai/investor-search-for-gemini
```

**Cursor** — Customize → Plugins → From GitHub Repository, then paste this repository's URL.

**Antigravity, Claude Code, GitHub Copilot** — copy the skill folder:

```
.agents/skills/investor-search/
```

into your project, or into `~/.agents/skills/` to have it available everywhere.

## What it does

Ask for the investors in a country, region or sector. You get one Excel file in which each
field records the page it came from.

It works to tell real investors apart from the advisers who sell to them, asks for proof
before treating two entries as the same firm, searches until six rounds in a row find
nothing new, and keeps its working files so a second run continues instead of repeating.

Where it cannot verify something, it records that rather than filling the gap.

## What it needs

A way to search the web, a way to fetch a page, and `python3`. In Gemini CLI those are
`google_web_search`, `web_fetch` and `run_shell_command`, all built in. No account, no API
key, no database.

Research only — not investment advice.

## Layout

| Path | Read by |
|---|---|
| `gemini-extension.json` | Gemini CLI |
| `.cursor-plugin/plugin.json` | Cursor |
| `skills/investor-search/` | Gemini CLI, Cursor |
| `.agents/skills/investor-search/` | Antigravity, Claude Code, GitHub Copilot, Cursor |

The two skill folders are kept byte-for-byte identical. Any change goes into both.

## Licence

MIT-0. See LICENSE.

---

© 2026 BCP partners GmbH · [Privacy](https://www.bcpp.io/investor-search-privacy) · [Terms](https://www.bcpp.io/terms-and-conditions)
