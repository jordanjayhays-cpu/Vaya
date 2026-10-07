# Flag: the Bureau now lets foreigners extend visas online themselves

Found 2026-09-28. **This affects Vaya Desk — Visa and the film that sells it.**

## What the Bureau says

A Bureau of Immigration press release, published 12 November 2025, quotes Commissioner Joel Anthony Viado:

> "Our eServices portal allows foreigners to extend their visas and access several other services wherever they are. This is part of our ongoing modernization efforts to make immigration services more efficient, secure, and accessible."

And, in the Bureau's own words:

> "through the BI's eServices platform, foreigners can conveniently process their visa extensions and other immigration-related transactions online without having to visit an office in person."

Portal: **e-services.immigration.gov.ph**
Source: immigration.gov.ph/foreigners-may-now-extend-visas-online-bi/

## Why this matters

`OFFER.md` sells **Vaya Desk — Visa at PHP 2,500**, and the pitch on `visa.html` and in `briefs/02-visa-truth.md` ends on **"We file it. You keep the day."**

That line assumes the alternative is a day at the Bureau. If the alternative is twenty minutes on a website, PHP 2,500 is a harder sell and the line is close to misleading.

## What this does not do

It does not kill the product. Three things survive:

1. **Not every step is online.** An ACR I-Card involves biometrics, which is a physical appearance. **Confirm exactly which steps still require attending in person.** This is now a question for the agency, and it is in the Ascentium draft
2. **Knowing when and what to file is the actual value.** The 30-day stamp, the 59-day line, the annual report window, what triggers an ACR I-Card. Most people do not know a deadline exists until they have missed it
3. **Someone tracking your dates for you** is a different product from someone queueing for you

But the product is now **"we keep track of it and handle it"**, not **"we save you a day at the Bureau."**

## What has to change

- **`briefs/02-visa-truth.md`.** The film must tell people the online portal exists. That is not optional under the rule that Vaya publishes everything it knows and sells only what it does. A film that hides the free option to sell the paid one is exactly what `standards.html` forbids
- **`visa.html`.** The honest section should name eServices and say plainly who should just use it
- **`OFFER.md`.** The one-line pitch needs rewriting away from "you keep the day"
- **Re-check the price.** PHP 2,500 was set against a day of your time. Against twenty minutes online, it needs a different justification or a different number

## Verify before acting

The press release is dated November 2025 and is about a typhoon closing a field office, so **the online service may cover fewer transaction types than the quote implies.** Open e-services.immigration.gov.ph and see exactly what can and cannot be done there before rewriting anything. Ask Ascentium and FilePino the same question.

**Do not rewrite the pages until you have checked the portal yourself.** But do not shoot `The Visa Truth` until you have either.

---

## RESOLVED 2026-10-07: portal checked, pages rewritten

The portal itself would not load from this environment (connection reset, twice, both through Firecrawl and curl). **So it was verified from the Bureau's own release plus three independent guides that document the live flow**, not from the portal UI. Treat the table below as good but not first-hand, and **confirm it in person in landing week one**, which is when Jordan files his own extension anyway.

| Transaction | Status |
|---|---|
| **9A tourist extension**, first and subsequent, including the 6-month LSVVE | **Online.** Card, GCash or Maya. 2 to 3 business days when approved |
| **Visa waiver extension** | **Online.** Listed separately from the tourist extension |
| **Exit clearance, ECC-B** | **Online**, stated as available 24 hours |
| **Annual report**, 1 Jan to 1 Mar | **Conflicted.** The portal accepts it. Separate Bureau notices to ACR I-Card holders have said personal appearance is mandatory. **Unresolved** |
| **ACR I-Card**, required past 59 days | **In person.** Biometric capture, and physical collection |
| Anything triggering a hearing | **In person** |
| Record mismatch, portal returns "no record found" | **In person**, to update manual records |

Every guide to the portal also warns that it goes down. **Do not file on the last day of an authorised stay.**

### What was changed, same day

- **`visa.html`** rewritten. New headline: *"You can file it yourself online. Most people miss the date instead."* The portal URL is in the hero. A whole new section tables online versus in person. The price table carries a **"Filing it yourself on the Bureau's portal: Free, government fees only"** row above Vaya's own fee. The honest section opens by retracting the old claim in so many words
- **`briefs/02-visa-truth.md`** rewritten. The portal is now beat two and the spine of the film, screen recorded start to payment. Closing line is *"The filing is twenty minutes and it is free. Missing the date is a fine and a lawyer. We are only useful for the second one."* Added to "what not to do": do not leave the portal out, and do not claim the annual report question is settled
- **`OFFER.md`** amendment one. Desk repositioned as dates-free plus filings-the-portal-will-not-take. **Price left alone, with three costed options for Jordan**
- **`index.html`**, **`manila.html`**, **`PRODUCTS.md`** aligned. `manila.html` still said "the Bureau costs you a day"

### Still open

1. **The annual report contradiction.** Question one for the lawyer hour, ahead of mass media ownership
2. **The Desk price.** Jordan's, three options in `OFFER.md`
3. **Confirm the table in person.** Landing week one, when Jordan files his own
