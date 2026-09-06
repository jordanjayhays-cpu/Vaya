# Vaya — Voices Around Your Area

**This repo is the home of Vaya.** Site, copy, city pages, and project notes all live here.
Intended to serve at **https://vayanews.com** through GitHub Pages (custom domain in `CNAME`).
As of 2026-09-06 that domain still shows a Squarespace "Coming Soon" parking page and Pages is not enabled
on this repo yet. See Publishing below.

## What Vaya is

A local newsroom in every city worth moving to. Each city gets a journalist and a videographer
who live there, paid to show what it is actually like: the cost of a month, the neighborhoods,
the work stack, the culture, the investor's read, a week in the life.

Audience: movers, long-stay visitors, and investors sizing up a city.

Around the films sits the ecosystem: **Experiences** (tours, live in Manila), **Living** (guides
and a relocation concierge), and **Social** (community). The films are how people meet Vaya.
The ecosystem is how they live with it.

## Pages

| File | Page | Status |
|---|---|---|
| `index.html` | Vaya home: why, cities, what you get, ecosystem, who it's for, newsletter | Built |
| `manila.html` | Vaya Manila: first three films, Manila ecosystem, topics, Starter Kit signup | Built |
| `CNAME` | `vayanews.com` for GitHub Pages | Waiting on Pages + DNS |

Cities on the roadmap: Mexico City, Bali (both "coming soon" on the home page).

## How it's built

Plain HTML and CSS, no build step, no framework, no JavaScript dependencies. Fonts load from
Google Fonts (Plus Jakarta Sans, DM Mono). Every page carries its own `<style>` block.

Design tokens are duplicated at the top of each page. Keep them identical across pages:

Theme: **Hibiscus** (chosen 2026-09-06, open to change later).

- White ground with blush off-white cards, light and dark themes (`prefers-color-scheme` plus `data-theme`).
- `--signal` hibiscus red `#ff2d55` for links, primary actions, and the newsletter block.
- `--stamp` tangerine `#ff8a3d` for badges and section labels.
- One typeface, Plus Jakarta Sans, for display and body. DM Mono for labels and buttons.
- Rounded: 20px cards, 26px panels, pill buttons and inputs.
- `themes.html` shows the home page in the nine candidates that were considered. Working file, not linked from the site.
- Archivo for headlines, Newsreader for body, IBM Plex Mono for labels and buttons.

## Adding a city

1. Copy `manila.html` to `<city>.html` and change the title, coordinates, hero, and topics.
2. Keep the section order: hero, first three films, ecosystem, topics, Starter Kit, footer.
3. On `index.html`, move the city card from `coming soon` to `live` and point it at the new page.
4. Open both pages locally in a browser, in light and dark mode, before pushing.

## Publishing

Push to `main`. Once GitHub Pages is on, it serves the repo root at vayanews.com. There is nothing
to build. The go-live steps (enable Pages, the exact DNS records for Squarespace) are in `DEPLOY.md`.

## Research

`research/` holds sourced briefs: `media-playbook.md` (what Vox, Vice, Semafor, Puck, Morning Brew and others do for content and revenue, with takeaways for Vaya) and `manila-food-tours.md` (partner candidates for Vaya Experiences, nightlife landscape, and how tour partnerships are priced), `manila-revenue-model.md` (each Manila video series paired with the revenue service it feeds, with a 90-day sequence), `how-they-started.md` (origin stories of Vox, Vice, Eater, Time Out, Fever and others, plus the Vaya project list in revenue-first order), `vaya-series.md` (the Manila season one slate and the paid thing behind each series), `game-plan.md` (the Airbnb-meets-Vox-and-Vice plan: hosts program, flywheel, economics, team, phases), `manila-demand.md` (sourced data on arrivals, nomads, retirees, expats, and how Manila compares to Bangkok, Bali and Mexico City), `vaya-series-v2.md` (the slate and revenue streams rebuilt on that data, plus the per-city demand-pass rule), `manila-month.md` (the 30-day stay product for remote workers, with the personal driver service priced), `visitor-mvps.md` (ten visitor pain points, the zero-build service for each, and the video that segues into it), `visa-desk.md` (the extension-filing service: rules, partner model, pricing), `vaya-care.md` (private nurse and household staff through Placewell, with the Philippines versus US and UK cost comparison), `story-briefs.md` (fourteen real-person stories to find, the service each sells, and where to find them), and `launch-checklist.md` (how Defector, 404 Media, Semafor and others actually launched, plus the email, legal, insurance and disclosure mechanics to have in place first).

## Forms

The newsletter and Starter Kit forms are static markup with no backend wired yet. Hooking them to
a list provider is the next open item.
