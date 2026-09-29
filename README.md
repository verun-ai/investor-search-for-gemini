# Investor Search

A Gemini CLI extension that builds a sourced list of the investors in any market:
family offices, VCs, PE firms and angels, where every firm carries the page it came from.

By **BCP partners GmbH** · [bcpp.io](https://www.bcpp.io)

## Install

```
gemini extensions install https://github.com/verun-ai/investor-search-for-gemini
```

Or install the skill on its own:

```
gemini skills install https://github.com/verun-ai/investor-search-for-gemini.git --path skills/investor-search
```

## What it does

Ask for the investors in a country, region or sector. You get one Excel file where every
field carries the page it came from.

It separates real investors from the advisers who sell to them, never merges two firms
without proof, searches until six rounds in a row find nothing new, and keeps its working
files so a second run continues instead of repeating.

Where it cannot verify something, it records that rather than filling the gap.

## What it needs

A way to search the web, a way to fetch a page, and `python3`. In Gemini CLI those are
`google_web_search`, `web_fetch` and `run_shell_command`, all built in. No account, no API
key, no database.

## Licence

MIT-0. See LICENSE.

---

© 2026 BCP partners GmbH · [Privacy](https://www.bcpp.io/privacy-policy) · [Terms](https://www.bcpp.io/terms-and-conditions)
