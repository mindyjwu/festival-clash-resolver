# Festival Clash Resolver & Smart Route Planner

**Live:** https://mindyjwu.github.io/festival-clash-resolver/

An offline-first web app for music festival and convention attendees. Star the artists you want to see, set priorities, and it resolves overlapping sets, factors in physical stage-to-stage walking time, and generates a lightweight personal schedule you can save to your phone for low-connectivity festival grounds.

## What it does

1. **Setup** — pick from a built-in library of real EDM festivals and tours (Sep 2026 → 2027), or paste your own timetable (pipe rows, sectioned text, or JSON). Configure a stage transit matrix: walking minutes between every pair of stages.
2. **Prioritize** — star sets and rank them **High (Must See)**, **Medium (Want to See)**, or **Low (Backup)**.
3. **Dashboard** — a chronological timeline that:
   - highlights **overlap clashes** between starred sets
   - recommends which set to catch based on your priorities, with **split-set** suggestions when priorities tie (*"see A for the first half, then walk to B"*)
   - raises **transit warnings** when the gap between consecutive sets is shorter than the walk (*"🚨 Tight Squeeze: you'll miss the first 12 minutes of…"*)
   - exports a self-contained `my_festival_schedule.html` you can add to your home screen and use with no signal

## Library

Twelve real festivals on their real recurring calendar slots, with real stage names and headline-tier acts — Amsterdam Dance Event, EDC Orlando, Dreamstate, Countdown NYE, Ultra Miami, DGTL, EDC Las Vegas, Movement Detroit, Defqon.1, Tomorrowland, Creamfields, Electric Zoo — plus tour and club-night templates.

> Because the app is fully offline with no live feed, and 2027 set times and full lineups aren't officially released yet, the timetables are **representative and fully editable**. Paste an official timetable whenever one drops.

## Tech

Single self-contained HTML file. Pure HTML5, Tailwind (CDN), vanilla JavaScript — no build step, no server, no external API. State persists in `localStorage`. Time math uses minutes-past-midnight so sets that cross midnight resolve cleanly.

Design: black-and-white with brushed-silver and rose-gold metallic accents, an opening reveal, and a slow chrome sheen — all disabled under `prefers-reduced-motion`.

## Run it

Open `index.html` in any modern browser. That's it.
