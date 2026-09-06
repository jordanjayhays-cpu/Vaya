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
- Theme is Hibiscus (see README). Design tokens are duplicated at the top of each page. Change them everywhere or nowhere.
- Voice: direct, concrete, first-hand. "The friend who already moved." No brochure language,
  no buzzwords, no em dashes.
- Every city page follows the Manila structure. Do not invent a new layout per city.
- Check light and dark mode before pushing. Pages go live on `main` with no review step.
- Anything only Jordan can do (domain, DNS, form backend, hiring correspondents, payments) goes
  on `agent_tasks` assigned `jordan`. If it is not on the board, it does not exist.

## Open items (as of 2026-09-06)

- Site is not live: GitHub Pages is off and vayanews.com points at a Squarespace "Coming Soon" parking page (Jordan).
- Newsletter and Starter Kit forms have no backend.
- No films published yet; every film card reads "coming soon".
- Mexico City and Bali pages do not exist.
