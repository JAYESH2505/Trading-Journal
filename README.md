# Process Log — Trading Journal

A single-file, browser-based trading journal built around one idea: **track whether you followed your rule separately from whether the trade won.**

No backend. No account. No dependencies. Your data never leaves your browser.

## Why this exists

Most trading journals only track P&L. That makes it easy to reinforce the wrong lessons — a lucky win (broke the rule, got away with it) looks identical to a good trade, and a disciplined loss (followed the rule, it just didn't work out) looks like a failure. Neither is true.

This journal splits every trade across two axes instead of one:

|                | **Win**            | **Loss**              |
|----------------|---------------------|------------------------|
| **Followed rule** | Disciplined win     | Disciplined loss (good process) |
| **Broke rule**    | Lucky win (flag this) | Undisciplined loss    |

The goal is to make it obvious, over time, whether the problem is your strategy or your discipline — because they need completely different fixes.

## Features

- Quick trade entry — instrument, direction, setup, entry/stop/exit with auto-calculated R-multiple
- Process × Outcome quadrant breakdown
- Equity curve (cumulative R across your trade sequence)
- Win rate, rule-adherence %, and expectancy at a glance
- Filterable trade history
- Export / import backups as JSON
- Runs entirely client-side — works offline once loaded

## Live site

`https://<your-username>.github.io/<repo-name>/`

*(replace with your actual GitHub Pages URL once it's live)*

## Getting started

### Use it online
Open the live site above. That's it.

### Run it locally
No build step, no install:
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```
Then just open `index.html` in a browser.

## How your data is stored

Trades are saved in your browser's `localStorage` — nothing is sent to a server. This means:

- Your data stays private to you by default
- It's tied to one browser on one device — clearing browser data, switching browsers, or moving devices will not carry it over
- Use the **Export backup** button regularly to save a `.json` copy, and **Import backup** to restore it or move it to another device

## Tech stack

Vanilla HTML, CSS, and JavaScript. No frameworks, no build tooling, no package.json. Fonts are IBM Plex Mono / IBM Plex Sans, loaded from Google Fonts.

## Roadmap ideas

- [ ] CSV export alongside JSON
- [ ] Multiple named rule sets, tracked separately
- [ ] Tag-level stats (which setups actually have edge)

## License

MIT — do whatever you want with it.
