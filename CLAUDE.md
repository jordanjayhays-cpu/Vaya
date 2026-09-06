# Working notes for Claude sessions — Vaya

**This repo is the home of Vaya.** Everything Vaya goes here: site pages, copy, city research,
scripts, and project notes. Do not file Vaya deliverables in `jordan-projects`; that repo only
carries a pointer to this one.

The system map (the board on Supabase `neurodashboards`, token discipline, operator rules) lives
in `mission-control/CLAUDE.md`. Read it before system-wide work.

## What this is

Vaya = Voices Around Your Area. A local newsroom per city (journalist plus videographer who live
there) telling movers, visitors, and investors what a city is actually like. Manila is the live
city. Mexico City and Bali are next. See `README.md` for pages, stack, and how to add a city.

## Rules that apply here

- Static site: plain HTML and CSS, no build step, no frameworks. Keep it that way unless Jordan
  says otherwise.
- Brand rules live in `BRAND.md` and the film rules in `kit/README.md` (graphics in `kit/`). Read them before writing copy or planning a shoot. When a brand or production rule changes in conversation, update these files in the same session; they are the living source of truth, and the published artifacts ("Vaya Brand Book", "Vaya Production Kit") are re-published from them.
- Theme is Hibiscus (see README). Design tokens are duplicated at the top of each page. Change them everywhere or nowhere.
- Voice: direct, concrete, first-hand. "The friend who already moved." No brochure language,
  no buzzwords, no em dashes.
- Every city page follows the Manila structure. Do not invent a new layout per city.
- No city gets a slate or a page before it gets a demand pass: `research/<city>-demand.md` first (who arrives, who has money, who is growing, what the constraint is), then the series and revenue mix are written against it. Manila skipped this and had to be redone (`research/vaya-series-v2.md`).
- Check light and dark mode before pushing. Pages go live on `main` with no review step.
- Anything only Jordan can do (domain, DNS, form backend, hiring correspondents, payments) goes
  on `agent_tasks` assigned `jordan`. If it is not on the board, it does not exist.

## Open items (as of 2026-09-06)

- `THIS-WEEK.md` is the execution list. No new research docs until it is done.
- Site is not live: GitHub Pages is off and vayanews.com points at a Squarespace "Coming Soon" parking page (Jordan).
- Newsletter and Starter Kit forms have no backend.
- No films published yet; every film card reads "coming soon".
- Mexico City and Bali pages do not exist.
