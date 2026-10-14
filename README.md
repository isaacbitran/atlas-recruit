# Atlas Recruit

Recruiting analytics for Brown Football. Live at [brownfootballmaps.org](https://brownfootballmaps.org).

Used daily by 25+ coaches and staff since fall 2025. Replaced 20+ hours a week of manual work.

This repo is a write-up. The code is private.

## What it does
- Where Ivy and FCS players come from: 13,000+ players, 2015–2026.
- Offer boards synced daily from the recruiting office's sheet.
- Retention and market-share analysis.
- A recruit-risk model.
- A chatbot over the data.

## How it's built
1. **App.** Next.js 16, React 19 and TypeScript on Vercel. One map component with modes (heat, counties, clusters, dots) over Mapbox GL and deck.gl.
2. **Data pipeline.** A daily GitHub Action pulls the offers sheet, geocodes only new schools, and keeps hand-audited coordinates.
3. **Rosters.** Roster history scraped each year, with identity resolution across seasons and tests for it.
4. **Chatbot.** Claude API, with Upstash Redis for feedback and state.
5. **Program as config.** A new program is a config, not a fork. Built to expand to CAA, Patriot League and MVFC schools with their own recruiting boards.

## History
Cold-approached the recruiting office as a freshman. Pitched the head coach two months later. v2 built by Archer, v3 (production) by me.

## Why it's private
The repo carries the program's recruiting board. Ask me for a walkthrough.
