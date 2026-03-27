# kestrel-roost

Tiny static site for the Kestrel roost page.

## Local preview

Because this site uses browser APIs (`localStorage`, `clipboard`), preview it through a local server instead of opening the file directly:

```bash
cd kestrel-roost
python3 -m http.server 8080
# then open http://localhost:8080
```

## What’s inside

- `index.html` — home page with quest generator + status widgets
- `game.html` — playable Sky Sprint mini-game
- `gallery.html` — image showcase wall
- `changelog.html` — release history + filterable flight log
- `quest-forge.html` — customize the quest generator pool (defaults + custom + JSON import/export)
- `flight-deck.html` — roadmap board + filterable ship log for visible product progress
- `notes.html` — searchable field-notes archive with tag filters + surprise picker
- `assets/` — image assets + shared JSON data for dynamic sections (`roost-updates.json`, `roost-notes.json`)

## New in this iteration

- **Field Notes page:** launched `notes.html` with full-text search, tag filters, and a “surprise me” interaction for browsing note cards
- **New content dataset:** added `assets/roost-notes.json` to keep writing/content updates data-driven (matching the existing updates system)
- **Homepage notes feed:** added a new “fresh field notes” card on `index.html` that pulls the latest entries from shared notes data
- **Sitewide navigation update:** linked the new Field Notes section from all major pages so the writing corner is discoverable

## Daily quest behavior

- Avoids repeating any of the last 3 rolled quests (when enough unique quests are available)
- Persists last quest, recent quest history, and accent in `localStorage` (with safe fallback when storage is unavailable)
- Shows live persistence status on the page (so users can tell when browser storage is blocked)
- Includes a “copy quest” button with secure-clipboard + legacy fallback support for wider browser compatibility
- Adds accessibility polish (`aria-live`, visible keyboard focus, reduced-motion handling)
- Supports keyboard shortcuts for quest actions (`R` roll, `C` copy, `A` accent, `S` reset streak)
- Tracks a UTC-based daily quest streak (increments once per day when you roll a quest)
- Keeps streak/reset timing accurate if the tab stays open across UTC midnight
- Shows a live countdown to the next UTC quest reset
- Stores a rolling history of the last 5 quest rolls with UTC timestamps
- Lets you click any history entry to restore that quest into the output
- Adds a manual “clear history” action to wipe quest history and reset the short repeat-avoid cache (without touching streak progress)
- Adds a manual “reset streak” button to restart the counter when needed
