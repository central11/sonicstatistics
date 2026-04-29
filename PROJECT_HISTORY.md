# SonicStatistics: Project History & Progress

This file serves as a persistent log of all major architectural decisions, UI refinements, and feature implementations for the SonicStatistics project.

## Project Vision
A Vignelli-inspired (Swiss International Style) dashboard for personal Spotify listening statistics, characterized by high contrast, bold typography (Google Sans), and a strict grid system.

## Core Infrastructure
- **API:** Supabase Edge Functions (`sonic-dashboard`).
- **Database:** Supabase (PostgreSQL) with migrations for tracking listening history and metadata cache.
- **Frontend:** Monolithic `index.html` in `hosted-dashboard/` (deployed via GitHub Pages/Netlify).
- **Data Collection:** Python-based poller (`spotify_listening.py`) syncing with Spotify API and Supabase.

## Major Milestones

### April 2026: UI & Interaction Refinement
- **Treemap Stability:** Refined the flexbox-based treemap to use `flex-basis` with minimum visibility thresholds (15%) and a strict `min-height` (100px).
- **Smooth Transitions:** Implemented `cubic-bezier` transitions and `will-change` properties to eliminate hover jitter.
- **Data Density:** Optimized section rendering to handle up to 15 items in treemap mode for better proportional representation.

## Technical Decisions
- **Color Extraction:** Real-time extraction of dominant colors from album art via `canvas` to style UI elements dynamically.
- **Session Management:** Password-to-session cookie flow (`sonic_session`) for private access.
- **Layout:** Strict grid system using CSS Grid for the main dashboard and refined Flexbox for proportional visualizations.

---
*Note: This file should be updated at the end of every session to ensure context continuity.*
