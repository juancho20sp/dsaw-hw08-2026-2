# HW08 — React Introduction

**Week 8 · DSAW · Universidad de La Sabana**

## Objective

Migrate the HW07 app to React, split it into components, and add a favorites feature.

## Setup

```bash
npm create vite@latest hw08 -- --template react
cd hw08
npm install
npm run dev
```

To deploy to GitHub Pages, install `gh-pages` and set the `base` option in `vite.config.js`.

## Deliverables

### React app in `src/`

Rebuild the HW07 app (public API + 3 states) in React with **at least 5 components** with descriptive names. Minimum example:
- `App.jsx` — root
- `SearchBar.jsx` — search input
- `ItemList.jsx` — results list
- `ItemCard.jsx` — individual card
- `LoadingState.jsx` / `ErrorState.jsx` — UI states

**Requirements:**
- Lists rendered with `.map()` and a unique `key` prop on each element
- Conditional rendering for all 3 states (loading, success, error)

### Favorites

- The user can mark/unmark items as favorites with a click
- Favorites are displayed in a separate section
- Implemented with `useState` — no Redux, no Context (yet)

## Layer 2

Favorites persist in `localStorage` — they survive a page reload.

## AI Log (`AI-LOG.md`)

- Did you ask AI to split the app into components? How did it decide where to split?
- Do you agree with that split? What would you change and why?

## Deployment

GitHub Pages with `gh-pages`:
```bash
npm install --save-dev gh-pages
# Add to package.json: "homepage": "https://YOUR_USERNAME.github.io/hw08"
# Add to scripts: "deploy": "gh-pages -d dist"
npm run build && npm run deploy
```

## Autograding

The pipeline will check:
- ✅ `package.json`, `src/App.jsx`, `src/` folder
- ✅ ESLint passes with no errors
- ✅ GitHub Pages responds
- ✅ 5 components, key props, favorites with state, 3 UI states (reviewed by Claude)

> **Submission rule:** If it is not deployed and public, it cannot be graded.
