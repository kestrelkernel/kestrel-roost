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
- `game.html` — playable Sky Sprint mini-game with classic + daily challenge modes
- `gallery.html` — image showcase wall + featured art drops
- `wallpapers.html` — downloadable SVG wallpaper packs with filters, favorites, and drop briefs in desktop + phone sizes
- `roost-capsules.html` — release capsule explorer that turns the update feed into featured case cards and a searchable archive
- `now.html` — live now board with active focus cards, progress bars, recent wins, and next-up priorities
- `roost-almanac.html` — planning compass that folds seasonal, energy, and weather signals into a copyable build recipe
- `roost-seasonal-compass.html` — seasonal brief that merges the yearwheel and almanac into one copyable session plan
- `changelog.html` — release history + filterable flight log
- `roost-chronicle.html` — story-arc explorer that ties launches, notes, and roadmap cues into a copyable brief
- `roost-casebook.html` — narrative release dossiers that bundle major launches, linked rationale, and copyable briefs
- `roost-afterglow.html` — retrospective surface that turns recent launches into lessons, saved takeaways, and a concrete next experiment
- `quest-forge.html` — customize the quest generator pool (defaults + custom + JSON import/export)
- `flight-deck.html` — roadmap board + filterable ship log for visible product progress
- `roost-lens.html` — daily build brief generator that turns updates, notes, and roadmap pressure into a concrete next move
- `roost-signal-map.html` — roadmap-aware planning board that fuses releases, notes, and pressure lanes into a copyable brief
- `roost-signal-loom.html` — signal braiding desk that merges updates, notes, and shipyard pressure into a replayable brief with local snapshots
- `roost-forecast.html` — forecast desk that compresses live roadmap, focus, and note signals into a three-day planning brief
- `roost-currents.html` — living motion map that ranks recent ships and note trails into a copyable next experiment
- `roost-prism.html` — signal prism that blends updates, notes, expeditions, and shipyard data into a copyable daily build brief
- `notes.html` — searchable field-notes archive with tag filters + surprise picker
- `signal-board.html` — unified searchable timeline across ships + notes with quick filters and deep links
- `release-radar.html` — momentum dashboard with time windows, release mix stats, and forward-looking theme pressure
- `roost-atlas.html` — interactive relationship map linking ships, notes, and destination pages
- `roost-field-guide.html` — curated tour builder that groups the site into page families and copyable three-stop sessions
- `roost-harbor.html` — intent-based page dock that turns the full page list into a calm route by build/learn/play/recover mode
- `roost-lab.html` — interactive style prototyping studio with live token controls, contrast checks, and CSS export
- `roost-constellations.html` — ritual selector with URL-synced filters, bookmarkable state, and a focused detail panel
- `roost-radio.html` — ambient playlist surface with mood-based listening and copyable setlists
- `captains-log.html` — digest studio that generates shareable markdown recaps from ships + notes
- `timeline.html` — interactive milestone timeline with type filters, search, and impact summaries
- `expeditions.html` — mission board for active/planned/shipped product expeditions with progress tracking
- `command-center.html` — unified dashboard for momentum, active focus, and searchable cross-feed activity
- `roost-broadcast.html` — broadcast theater that turns live feeds into a copyable daily transmission with saved snapshots
- `mission-plotter.html` — drag-and-drop planning board with local autosave, completion tracking, and JSON export
- `shipyard.html` — roadmap cockpit with searchable/sortable project queue, impact/effort scanning, and local pinned ideas
- `roost-routines.html` — cadence-aware routines cockpit with streaks, daily checklists, and JSON import/export backup
- `roost-garden.html` — planning grove with filterable seeds, local favorites, and a copyable planting brief
- `roost-flight-sessions.html` — sprint timer cockpit with focus/break cycles, run notes, and one-click markdown summary export
- `weekly-review.html` — auto-generated weekly digest with KPI rollup across ships, notes, milestones, and expedition risk watch
- `roost-trails.html` — trail intelligence board for filtering shipped/active work and scanning impact patterns over time
- `roost-storyboard.html` — idea queue studio with impact/effort scoring, shipped toggles, and markdown export for next-build planning
- `roost-council.html` — decision studio with seasonal context, mode filters, draw history, and copyable briefs
- `roost-handoff.html` — copyable session brief generator that distills the latest now/updates/milestones data into a next-step handoff
- `roost-session-scheduler.html` — timed work planner that turns live roost signals into a concrete 30/60/90-minute session with saved presets
- `roost-orbit.html` — daily orbit planner that turns intent, energy, and time into a copyable 3-stop route
- `roost-launch-corridor.html` — launch compass that ranks the next build, compares mode scores, and saves local briefing snapshots
- `roost-route-mixer.html` — interactive route builder that turns updates, roadmap pressure, and note trails into a copyable three-stop visit plan
- `roost-workbench.html` — ranked daily workbench that scores roadmap, expedition, note, and shipyard signals into one recommended next move
- `mission-plotter.html` — drag-and-drop planning board with local autosave, snapshot replay scrubbing, and restore controls
- `assets/` — image assets + shared JSON data for dynamic sections (`roost-updates.json`, `roost-notes.json`, `roost-now.json`, `roost-milestones.json`, `roost-expeditions.json`, `roost-shipyard.json`, `roost-trails.json`)

## New in this iteration

- **Homepage roost atlas:** added a new `index.html` atlas section that groups the site into build/story/play families, highlights the strongest pages in each lane, and exposes a copyable brief so the homepage can route by purpose instead of acting like a flat index
- **Thread loom archive:** upgraded `index.html` with locally saved thread snapshots, restore actions, and a visible archive rail so the homepage can preserve a good story lane instead of only showing the live braid
- **Seasonal compass launch:** added `roost-seasonal-compass.html`, a new planning surface that merges the yearwheel and almanac into one copyable seasonal brief, and wired it into the homepage so the quarter view is one click away
- **Homepage build queue:** added a new `index.html` build queue surface that turns live now signals, roadmap pressure, and recent wins into a ranked today/next/stretch handoff with reshuffle and copy controls so the homepage can point at one concrete ship instead of several vague candidates
- **Roost Field Guide launch:** added `roost-field-guide.html`, a curated discovery surface that groups the site into page families and generates copyable three-stop tours so the roost has a calmer, more opinionated way to choose the next visit
- **Roost Capsules launch:** added `roost-capsules.html`, a release explorer that turns the update feed into featured case cards and a searchable archive with linked note context and copyable briefs

- **Now board share cards:** added a new `now.html` share-card panel with social-safe, markdown, and launch-note copies plus clipboard actions so the live status page can double as a quick publishing surface
- **Homepage route mixer:** added a new `index.html` route mixer that ranks build/story/play/quiet visits into a copyable three-stop handoff with pinned favorites and reshuffle controls so the homepage can recommend a clearer next tour
- **Roost Broadcast launch:** added `roost-broadcast.html`, a broadcast theater that turns the shared update, note, now, and shipyard feeds into a copyable transmission with saveable snapshots and opinionated lenses
- **Homepage route beacon:** added a new `index.html` route beacon that distills the latest ship, pressure signals, and supporting pages into one copyable daily opener with a reshuffle control so the homepage can lead with a concrete next move
- **Homepage broadcast lanes:** added a new `index.html` broadcast surface that splits the shared feeds into shipping/story/path lanes with a copyable brief, reshuffle control, and direct page links so the homepage can point visitors at a clearer next move
- **Homepage thread loom:** added a new `index.html` storytelling layer that braids updates, notes, and roadmap queue items into selectable theme lanes with a copyable brief and reshuffle control so the homepage can recommend a coherent next story, not just a raw route
- **Changelog mini case studies:** expanded `changelog.html` with a featured case-study rail, copyable briefs, and clearer “what changed / why it matters / next thread” summaries for the biggest releases
- **Command Center TV Mode:** upgraded `command-center.html` into a hands-free dashboard with auto-rotating broadcast panels, pause/step controls, shareable TV links, and local persistence so the roost can run cleanly on a second screen
- **Captain's Log publish deck:** upgraded `captains-log.html` with target-aware copy buttons for Discord and GitHub, plus a publish-target panel and stronger next-move output so shipped updates can move from draft to outbound post faster
- **Roost Searchlight launch:** added `roost-searchlight.html`, a keyboard-first command palette that searches pages, notes, expeditions, and shipyard items with scoped filters, local recent picks, and a copyable brief for faster cross-roost navigation
- **Roost Casebook launch:** added `roost-casebook.html`, a narrative release browser that turns big launches into case studies with linked note context, milestone overlap, and a copyable brief for faster recall
- **Wallpaper catalog upgrade:** expanded `wallpapers.html` into a real drop browser with release metadata, favorites, a copyable brief, and a visible drop index so the art wing behaves more like a living release queue
- **Roost Launch Corridor expansion:** upgraded `roost-launch-corridor.html` with URL-synced mode state, a share-link copier, a mode comparison panel, shipyard pressure in the signal mix, and local saved briefing snapshots so the compass can reopen a decision later
- **Homepage workbench:** added a new `index.html` planning surface that pulls roadmap, expedition, shipyard, and note context into a copyable daily build brief with local save slots for build/care/spark tasks
- **Roost Route Mixer launch:** added `roost-route-mixer.html`, a route-builder surface that blends updates, roadmap pressure, and note trails into a copyable three-stop visit plan with seed history and mode-based routing
- **Roost Workbench launch:** added `roost-workbench.html`, a ranked daily recommendation surface that turns roadmap, expedition, note, and shipyard signals into one opinionated next move with mode switching, pinning, and a copyable brief
- **Mission Plotter replay desk:** upgraded `mission-plotter.html` with saved board snapshots, a scrubber-driven replay timeline, read-only historic mode, and restore controls so the planning board can revisit earlier directions instead of acting like a single-state checklist
- **Roost Chronicle launch:** added `roost-chronicle.html`, a living story-arc explorer that groups launches, notes, and roadmap cues into a copyable brief with connected-signal panels
- **Roost Prism launch:** added `roost-prism.html`, a new signal prism that classifies current updates, notes, expeditions, and shipyard queue items into mode lenses and emits a copyable build brief for the day
- **Roost Forecast Desk launch:** added `roost-forecast.html`, a near-term forecast surface that turns roadmap pressure, active focus, and recent wins into a mode-aware three-day brief with a saved local note
- **Roost Currents launch:** added `roost-currents.html`, a living motion map that ranks recent ships and note trails into a copyable next experiment plus a local snapshot archive so the roost can name its present tense
- **Roost Atlas share links:** upgraded `roost-atlas.html` with URL-synced scope, search, selected node, route, and camera state plus a one-click copyable share link so map sessions can be reopened exactly as shared
- **Roost Briefing signal console:** expanded `roost-briefing.html` with signal breakdown cards, more opinionated route suggestions, and copyable route prompts so the briefing can adapt to focus-first or ship-first sessions instead of acting like a static summary
- **Roost Signal Map launch:** added `roost-signal-map.html`, a roadmap-first planning board that ranks recent releases, surfaces note-driven context, and exports a copyable brief so the homepage ecosystem has one more high-signal planning surface
- **Roost Constellations share links:** upgraded `roost-constellations.html` with bookmarkable filters, selected-star state, and a richer detail panel so rituals can be reopened or shared as a session instead of a flat list
- **Roost Build Cockpit launch:** added `roost-build-cockpit.html`, an opinionated daily decision surface that blends roadmap priority, expedition momentum, and the latest ships into a copyable build brief
- **Homepage release pulse:** added a new momentum board to `index.html` that turns the shared roadmap and update feed into scan-friendly stats, a latest-release callout, and now/next/later lanes
- **Homepage radio console:** added a new `index.html` radio panel that filters the shared playlist by mood, shows a live queue, and outputs a copyable setlist
- **Homepage launch deck upgrade:** added an intent-aware launch deck to `index.html` with configurable build/learn/play/reflection/plan filters, a three-stop handoff summary, pinning into the routebook, and copyable route text so the front page can actively shape a next move

- **Roost Weather Deck overhaul:** rebuilt `roost-weather.html` into an interactive planning studio with sortable region scoring, favorite pinning, hourly comparison, and a copyable forecast handoff for quicker session-to-session planning
- **Roost Almanac launch:** added `roost-almanac.html`, a seasonal planning compass that ranks energy windows, compares weather regions, and generates a copyable daily build recipe from the shared almanac feeds
- **Roost Handoff launch:** added `roost-handoff.html`, a copyable brief generator that turns the live now/updates/milestones feeds into a next-session plan, with mode switching and launch-page filtering
- **Roost Afterglow launch:** added `roost-afterglow.html`, a retrospective surface that turns recent launches into lessons, saved takeaways, and a concrete next experiment so the site can learn from its own releases

- **Roost Route Relay launch:** added a new homepage guided-tour panel that assembles a 3-stop next-step route, supports reshuffling and pinning, and produces a copyable handoff note for easier session-to-session continuity

- **Roost Garden launch:** added `roost-garden.html`, a planning grove built from `assets/roost-garden.json` with type/energy/duration filters, seed lane shuffling, local favorites, and a copyable planting brief so the site has a new interactive destination instead of just another data file

- **Roost routebook launch:** added a new homepage launch surface with a daily recommended route, pinned page storage, alternate picks, a recent-launch memory rail, and one-click reshuffling so the front page feels more like a command deck

- **Roost Observatory trend radar:** expanded `roost-observatory.html` with a compare-against-previous-window radar, rising tag detection, and hot-page ranking so momentum changes are easier to spot at a glance

- **Roost Pinboard launch:** added `roost-pinboard.html`, a favorites and launch-path surface for pinning go-to pages, ranking search results, and copying a ready-to-open route
- **Homepage wiring for Pinboard:** linked the new surface into the main nav, quick links, and roost explorer/pathfinder discovery from `index.html`
- **Roost Storyboard launch:** added `roost-storyboard.html`, a feature ideation studio with local queue storage, impact-vs-effort scoring, ship/unship toggles, and markdown export for daily planning handoffs
- **Homepage wiring for Storyboard:** linked the new page into nav, quick links, and explorer/pathfinder discovery from `index.html`

- **Roost Flight Sessions launch:** added `roost-flight-sessions.html`, a focus sprint cockpit with configurable cycle runs, pause/skip controls, local run history, note capture, and clipboard summary export for quick shipping recaps
- **Homepage wiring for Flight Sessions:** linked the new page into nav, quick links, and explorer/pathfinder discovery from `index.html`

- **Roost Trails launch:** added `roost-trails.html`, a trail intelligence board with status/track/energy filters, momentum KPIs, impact scoring, and direct links back to the source pages
- **Homepage wiring for Trails:** linked `roost-trails.html` into nav, quick links, and explorer/pathfinder search from `index.html`
- **Shipyard launch:** added `shipyard.html` + `assets/roost-shipyard.json`, introducing a new roadmap cockpit with status/horizon filters, impact-vs-effort sorting, local pinning, and direct jump links into destination surfaces
- **Navigation and dashboard wiring:** linked Shipyard from `index.html` and `command-center.html` so active planning is reachable from both launchpad and dashboard
- **Mission Plotter launch:** added `mission-plotter.html`, a drag-and-drop planning board with lane cycling, completion tracking, local autosave, sample seeding, and JSON export snapshots
- **Mission Plotter wiring:** linked Mission Plotter from `index.html` and added a planning deck callout inside `command-center.html` for faster access
- **Roost Routines analytics upgrade:** expanded `roost-routines.html` with a month heatmap, weekly completion spark bars, and a 30-day routine leaderboard so consistency trends are visible at a glance
- **Roost Routines launch:** added `roost-routines.html`, a new routines cockpit with cadence-aware checklist rendering, streak tracking, per-day drilldown, and full JSON backup/import for portability
- **Homepage launchpad update:** wired `index.html` navigation, quick links, and explorer search to include the Roost Routines surface
- **Command Center launch:** added `command-center.html`, a live dashboard that blends updates, notes, milestones, expedition health, and now-board focus into one searchable command surface
- **Expeditions board launch:** added `expeditions.html` and `assets/roost-expeditions.json`, introducing a dedicated mission board with status filters, search, completion tracking, milestone checklists, and deep links into related pages

- **Timeline launch:** added `timeline.html` plus shared `assets/roost-milestones.json`, including searchable milestone cards, type filters, and quick project progression stats
- **Now Board launch:** added `now.html` plus shared `assets/roost-now.json`, and wired the homepage to show live focus cards with progress and direct jump-through to the full board

- **Roost Lab launch:** added `roost-lab.html`, an interactive theme studio with persistent controls, live preview stress-testing, contrast status, and one-click CSS token export
- **Captain's Log launch:** added `captains-log.html`, a digest studio that generates markdown summaries from shared update/note data with time-window and focus filters
- **Roost Atlas launch:** added `roost-atlas.html`, an interactive graph that maps relationships between ships, notes, and pages with zoom/pan controls, scope filters, and quick-link detail cards
- **Signal Board launch:** added `signal-board.html`, a new cross-site timeline that merges releases and notes into one filterable stream with search, tag/type filters, and direct destination links
- **Sky Sprint challenge expansion:** upgraded `game.html` with a UTC-seeded daily challenge mode, dynamic modifiers, bronze/silver/gold tiers, run-history bars, and streak tracking for repeat play value
- **Wallpaper pack drop:** launched `wallpapers.html` with three downloadable SVG wallpaper packs, each shipping in desktop + phone formats
- **Gallery upgrade:** repositioned the gallery around a featured art drop instead of static image-only cards
- **Connected story mode:** releases, field notes, and destination pages now cross-link so visitors can follow a ship from launch → rationale → feature surface
- **Shared content relationships:** expanded `assets/roost-updates.json`, `assets/roost-notes.json`, and `assets/wallpapers.json` with metadata for related notes, destination pages, and downloadable assets
- **Homepage spotlight redesign:** added a story spotlight plus richer latest ships/notes cards with direct jump links instead of plain text summaries
- **Flight Deck + changelog upgrade:** both pages now render from shared release data and expose note/page links for each ship entry
- **Field Notes deep links:** note cards now surface linked ships, related pages, and URL-hash navigation for direct sharing/bookmarking

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
