# Hero Wars

A small browser game starring the team's superheroes. In **Weakness Wars**, every villain is born from one hero's weakness — your job is to send in the hero who can beat it.

## Play

Open `index.html` in a browser. No build step, no dependencies (fonts load from Google Fonts; without a connection the page falls back to system fonts).

To host it, enable GitHub Pages for this repo (Settings → Pages → deploy from the `main` branch, root folder).

## Rules

- 10 villains appear in random order, one per hero weakness.
- Pick one of the 10 heroes for each villain:
  - **Perfect match:** +100
  - **Solid pick:** +50
  - **Any other hero:** 0
  - **The hero whose own weakness it is:** −25
- Every hero is the perfect match for exactly one villain, so the maximum is 1000 points.
- Your best score is remembered in your browser.

## The heroes

| # | Hero | Role | Weakness |
|---|------|------|----------|
| 01 | Mr. Research | Keeper of the research data | Unlabelled columns |
| 02 | Mr. Handoff Plugin | Passes data between apps | Breaking API changes |
| 03 | Mr. Sekretariat | Master of processes | "Can you just quickly…" |
| 04 | Mr. DevOps | Leader of the DevOps Guild | Flaky tests |
| 05 | Mr. Power BI | Dashboard wizard | Data refresh failed |
| 06 | Mr. MESI | Guardian of Multi Entity Single Instance | Hard-coded entity IDs |
| 07 | Mr. Flughafentaxi | The family airport shuttle | Last-minute flight changes |
| 08 | Mrs. Coordinator | Avaloq tickets, releases & Pikett | Tickets with no description |
| 09 | Mr. Salesforcechat | The one-man integration team | Tickets stuck in "Waiting" |
| 10 | Mr. Gleitschirm | Our high-flying apprentice | Rainy weekends |

The full hero cards are in [`cards/`](cards/); the small portraits used in the game are in [`assets/avatars/`](assets/avatars/).

## Changing the game

All game data lives in the `VILLAINS` and `HEROES` arrays near the top of the script in `index.html`. Each villain has:

- `nem` — the hero whose weakness it is (−25)
- `best` — the perfect hero and the story line shown on a win (+100)
- `ok` — the solid backup and its story line (+50)

The answer key is in [`SOLUTIONS.md`](SOLUTIONS.md) — spoilers.
