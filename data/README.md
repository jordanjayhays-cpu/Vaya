# data/

Structured contact data harvested from public sources. **Not lead lists to blast.**

## manila-tour-guides.csv

DOT-accredited tour guides, harvested from the Intramuros Administration's public directory at `intramuros.gov.ph/guides/` on **2026-09-28**. Every field is published by the Administration for the express purpose of letting visitors hire these guides.

**The `status` column is the only one that matters first.**

| status | meaning |
|---|---|
| `CURRENT` | Accreditation valid beyond today. Contactable |
| `EXPIRED` | Accreditation lapsed. **Ask whether they have renewed before anything else** |
| `NO_CONTACT_PUBLISHED` | Listed in the directory, no contact block on the profile |

**Roughly one in three is current.** The newer accreditation numbers (the 04xxx series, issued 2025 and 2026) are the live ones. The 003xx and 009xx series from 2021 have almost all lapsed.

## Rules for using this file

1. **Do not mass-mail it.** These are individual freelancers. The Manila guiding community is small and a spray would be noticed. Three considered emails beat ninety identical ones
2. **Check the expiry on the profile page before contacting**, because this snapshot ages
3. **Whether DOT accreditation is legally required** to guide a paid tour, or is voluntary and reputational, is an open question for the lawyer hour. It decides whether `EXPIRED` disqualifies someone
4. **Language is a product, not a footnote.** Spanish, Italian, Mandarin and Japanese speakers are each a different offer, not a backup for the English one

## Source
- Directory: intramuros.gov.ph/guides/
- Directory contact: tourism@intramuros.gov.ph
- Each row read from that guide's own profile page
