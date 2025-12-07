# Pokedex Lite

A lightweight Pokedex web app built with React + Vite. Implements listing, search, type-filtering, pagination, favorites (localStorage), and a detail modal.

## Features
- Fetches Pokémon list from PokéAPI.
- Search by name (live filtering).
- Filter by type (multi-select).
- Pagination (load next/previous pages).
- Favorite Pokémon persisted in localStorage.
- Detail modal with stats and abilities.
- Responsive design (mobile / tablet / desktop).

## Run locally
1. Install dependencies:

```bash
npm install
```

2. Start dev server:

```bash
npm run dev
```

Open http://localhost:5173 (Vite default) in your browser.

## Build for production

```bash
npm run build
npm run preview
```

## Why these tech choices
- **React + Vite**: fast dev server and minimal setup. No external UI libs used so code is original and easy to read.

## Notes & Challenges
- The PokéAPI doesn't return high-res images in the paginated endpoint; we fetch each Pokémon's details when needed to show the artwork.
- To avoid too many network calls we fetch detail data on demand and cache it in component state.
