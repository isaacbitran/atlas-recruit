# Atlas Recruit

Recruiting analytics used daily by Brown Football's coaches and staff (25+ people) since fall 2025. Live at [brownfootballmaps.org](https://brownfootballmaps.org).

It replaced 20+ hours a week of manual work. This repo is a write-up; the code is private.

## What it does
- **Maps** where Ivy and FCS players come from: 13,000+ players, 2015–2026.
- **Offer boards** synced daily from the recruiting office's sheet.
- **Retention and market share** by region and program.
- **Recruit-risk model.**
- **Chatbot** over all of the above.

## How it works
1. **One map, many modes.** A single component switches between heat, county, cluster and dot views over Mapbox GL and deck.gl.
2. **Daily pipeline.** A GitHub Action pulls the offers sheet, geocodes only new schools, and keeps hand-audited coordinates.
3. **Roster history.** Rosters are scraped each year, with tested identity resolution across seasons.
4. **Chatbot.** Claude API, with Upstash Redis for feedback and state.
5. **Program as config.** A new school is a config, not a fork. Built to expand to CAA, Patriot League and MVFC programs with their own recruiting boards.

## Stack
Next.js 16, React 19, TypeScript, Tailwind, Mapbox GL, deck.gl, Claude API, Upstash Redis, GitHub Actions, Vercel.

## History
I cold-approached the recruiting office as a freshman and pitched the head coach two months later. Archer built v2; I built v3, the production version.

## Why it's private
The repo carries the program's recruiting board. Ask me for a walkthrough.
