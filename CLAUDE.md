# CLAUDE.md — NorCal Trackdays

## Project Overview

CA Track Day Schedule 2026 — a single-page web app listing motorcycle, car/HPDE, and school track day events at three Northern California racetracks: Laguna Seca, Sonoma Raceway, and Thunderhill.

## Tech Stack

- **Static HTML/CSS/JS** — no build tools, no framework, no dependencies
- **Fonts**: Google Fonts (Bebas Neue, DM Mono, DM Sans)
- **Styling**: CSS custom properties, dark theme, responsive (mobile breakpoint at 768px)
- Open `index.html` directly in a browser to run

## Project Structure

```
index.html    — Full application: markup, styles, and JavaScript in a single file
CLAUDE.md     — This file
```

## Architecture

### Data
- All event data lives in a `const events` array in the `<script>` block of `index.html`
- Each event object has: `date`, `end` (optional, for multi-day), `track`, `event`, `organizer`, `type`, `price`, `url`
- Events are organized by track (Laguna Seca, Sonoma Raceway, Thunderhill) then by type (School, Car/HPDE, Motorcycle)

### Tracks (color-coded)
- **Laguna Seca** — gold (`#e8b84b`)
- **Sonoma Raceway** — blue (`#5ba3f5`)
- **Thunderhill** — red/coral (`#f07050`)

### Event Types
- **Motorcycle** — purple (`#a87eff`)
- **Car / HPDE** — green (`#4ecda4`)
- **School** — orange (`#ff9f55`)

### Filtering & Sorting
- Three independent filter groups: Track, Type, Weekday/Weekend
- Track filter uses radio-style (one active at a time, or "All")
- Type and Day filters are toggleable (click again to deselect)
- Sorting by date (default), track, or organizer — via dropdown or clickable column headers

### Rendering
- `render()` function filters, sorts, and rebuilds the `<tbody>` on every interaction
- No virtual DOM or diffing — direct `innerHTML` replacement

## Development Guidelines

### Adding Events
Add new event objects to the `events` array in `index.html`, following the existing format:
```js
{ date:"YYYY-MM-DD", end:"YYYY-MM-DD", track:"Track Name", event:"Event Title", organizer:"Org Name", type:"Motorcycle|Car / HPDE|School", price:"$XXX", url:"https://..." }
```
The `end` field is optional (omit for single-day events).

### Git Workflow
- Commit messages should be concise and describe the "why" of the change
- Keep commits focused — one logical change per commit

### AI Assistant Notes
- Always read `index.html` before modifying it — all code lives in this single file
- Preserve the existing dark theme and color conventions when adding UI elements
- Event data sources are listed in a comment block above the `events` array
- Do not split the file into separate CSS/JS files unless explicitly requested
