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
Google Fonts (Archivo, Newsreader, IBM Plex Mono). Every page carries its own `<style>` block.

Design tokens are duplicated at the top of each page. Keep them identical across pages:

- White ground with warm off-white cards, light and dark themes (`prefers-color-scheme` plus `data-theme`).
- `--signal` (Virgin-style red `#e3162b`) for links, primary actions, and the newsletter block.
- `--stamp` (coral `#ff7a45`) for badges and section labels.
- `palette.html` shows the current scheme next to two alternatives (Sunset, Red on cream). Not linked from the site.
- Archivo for headlines, Newsreader for body, IBM Plex Mono for labels and buttons.

## Adding a city

1. Copy `manila.html` to `<city>.html` and change the title, coordinates, hero, and topics.
2. Keep the section order: hero, first three films, ecosystem, topics, Starter Kit, footer.
3. On `index.html`, move the city card from `coming soon` to `live` and point it at the new page.
4. Open both pages locally in a browser, in light and dark mode, before pushing.

## Publishing

Push to `main`. Once GitHub Pages is on, it serves the repo root at vayanews.com. There is nothing
to build. To go live, Jordan needs to:

1. Enable Pages on this repo (Settings > Pages > Deploy from branch `main`, folder `/`).
2. Point vayanews.com DNS (managed at Squarespace) at GitHub Pages: A records to GitHub's Pages IPs, plus a CNAME for `www`.
3. Confirm the custom domain in the Pages settings and turn on Enforce HTTPS.

## Forms

The newsletter and Starter Kit forms are static markup with no backend wired yet. Hooking them to
a list provider is the next open item.
