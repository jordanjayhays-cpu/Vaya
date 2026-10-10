# The funnel: film to money

Written 2026-10-10. **This traces one viewer from a film they have not seen yet to a service they have not bought yet, and marks every point where the chain is currently cut.**

The short version: **eleven links, three are broken, and one of the three is five minutes of your time.**

---

## The chain, link by link

| # | Link | Status | Owner |
|---|---|---|---|
| 0 | **A film exists** | **CUT.** Zero published. EP01 in production, four not started | Jordan, January |
| 1 | **A viewer finds it** | **CUT.** No YouTube channel exists. Nothing in this repo references one | Jordan |
| 2 | **The end-card names a URL and a code** | **FIXED TODAY.** One numbering, EP01 to EP05 | Done |
| 3 | **The URL resolves** | **WORKS.** Verified 10 Oct | Done |
| 4 | **The page matches the film** | **FIXED TODAY.** Code on the page now equals code on the card | Done |
| 5 | **The page gives something away free** | **WORKS** | Done |
| 6 | **There is one obvious thing to click** | **WORKS.** 17 CTAs across 11 pages | Done |
| 7 | **The click reaches a human** | **CUT. FATAL.** `hello@vayanews.com` does not exist. **All 17 CTAs bounce** | **Jordan, 5 min** |
| 8 | **A quote goes back** | Works once link 7 exists | Jordan |
| 9 | **The customer can pay** | **CUT.** No payment rail anywhere | Jordan |
| 10 | **Somebody delivers it** | **CUT.** No signed partner for any of the four products | Jordan |
| 11 | **The result becomes proof** | Nothing to prove yet | January |

---

## Link 2, 3 and 4: what was actually wrong, and what I changed

**The numbering was running two systems against each other.** `kit/README.md` says episode codes start at EP01 and go on from there, and that the code appears on the receipt end-card, in the description link and in the email subject. The brief filenames agreed. The homepage cards agreed. **The four service pages did not: they were one ahead.**

| Film | Homepage said | Page and brief said | Now |
|---|---|---|---|
| Block by Block, Makati | 01 | no code at all | **EP01** |
| The Visa Truth | 02 | EP03 | **EP02** |
| What happens when you land at NAIA | 03 | EP04 | **EP03** |
| Eat Here, Not There | 04 | EP05 | **EP04** |
| Five days to a home in Makati | 05 | EP06 | **EP05** |

**Why this mattered more than it looks.** The code is the only attribution Vaya has. A viewer sees **EP02** on the receipt end-card, lands on `/visa`, and the email button fills in the subject `Visa Desk EP02`. **That subject line is the entire mechanism for knowing which film earned the money.** With the page running one ahead, a film would have said EP03 and the homepage would have said 02 for the same thing, and the first time anyone asked "which film sold that" the answer would have been a guess.

**It was free to fix today and it will not be free later.** Nothing outside this repo references the old codes, because no film is published. The moment EP02 goes out on a thumbnail, the number is permanent.

**Three other things fixed in the same pass:**

- **Five dead play buttons.** Every film card had a red 52px play circle on a `div` with no link behind it. Five of them, none playing anything. Unpublished films now show their episode code in the thumbnail instead. The CSS carries a comment saying exactly what to swap back when a film goes live
- **The flagship had nowhere to send anyone.** `briefs/01` says no call to action, which is right, and the homepage card said "Nothing to sell" as dead text. **An audience with nowhere to go evaporates.** The card and the end-card now both point at `vayanews.com/starter-kit`, the free guide that asks for nothing. The one film with nothing to sell points at the one page that sells nothing
- **`vayanews.com/visa` works, and so does every short URL.** Checked live: `/`, `/visa`, `/landing`, `/food-tour`, `/move-in`, `/starter-kit`, `/manila` all return 200 without the `.html`. **This was the single biggest unverified assumption in the whole plan**, because three briefs put a short URL on screen and an extensionless 404 would have killed the funnel at link 3 with no way to tell from the film side

---

## Link 7: the five-minute fix that unblocks everything

`hello@vayanews.com` is the address on **every** call to action on the site. It is an alias, it is free, it takes about five minutes in Google Workspace, and **it does not exist**, so right now every button on the site produces a bounce.

Seventeen CTAs across eleven pages, all pointing at a dead mailbox:

| Page | What the button promises |
|---|---|
| `visa.html` | Your visa dates back the same day, free, twice on the page |
| `landing.html` | Start a Landing booking, twice |
| `food-tour.html` | Start a tour booking, twice |
| `move-in.html` | Start a Move In, twice |
| `index.html`, `manila.html` | Go on the newsletter list |
| `standards.html`, `terms.html`, `privacy.html` | A correction, a complaint, a privacy request, each promising a reply in two working days |
| `starter-kit.html`, `retire.html` | Report an out-of-date price |

**The ones on `standards.html` and `terms.html` are the worst of the set**, because they promise a reply within two working days on the pages that exist to establish that Vaya keeps its word.

---

## Link 9: the money, and a claim already live that is not true yet

**There is no way to pay Vaya.** No link, no account named, nothing on any page. The flow stops dead between "here is your quote" and "here is the work."

And `privacy.html` already states:

> We do not collect payment card details. Payments go through a payment provider and we never see the card.

**There is no payment provider.** In a privacy policy that reads as forward-looking rather than false, so this is not an emergency, but `standards.html` is built on Vaya not saying things that are not so. **Either pick a provider or soften the line.**

The constraint that actually decides it: **the customer is in the US or Europe, paying before they arrive, to a business with no Philippine entity yet.** That rules out most of the obvious local answers.

> **BOARD: pick one payment method for the first ten customers.** Not the permanent answer, the one that lets a stranger pay you in January. Three shapes, and this is yours:
> 1. **An invoice with a bank transfer**, in your own name. Zero setup, zero fees to you, slow and high-friction for the customer, and it looks small
> 2. **Wise or a similar transfer account.** Near-zero setup, multi-currency, cheap, still manual, still your personal name on it
> 3. **A card processor.** Highest trust and the only one that converts a stranger on a first visit. **Most of them want a registered business**, which you do not have until the lawyer answers question 6
>
> **This is on the critical path to the first peso and nothing in the repo addresses it.** Decide it before the price, because option 3 may be gated on the company structure.

---

## Link 10: nobody has agreed to deliver anything yet

`OFFER.md` already carries this table and nothing in it has moved:

| Product | Needs | Where it is |
|---|---|---|
| Desk, Visa | A signed BI-accredited agency | **Drafts in Gmail: FilePino, Ascentium. Unsent** |
| Concierge, Landing | A transport rate, eSIM tested end to end | **Drafts in Gmail: MTSC, VPI. Unsent** |
| Tours, Food | A guide's net rate, the route walked, insurance bound | **Drafts in Gmail: five guides, AIG. Unsent** |
| Home, Move In | A licensed broker, **and the RESA answer** | **Blocked on the lawyer** |

**So the funnel has a page and a price for four things that no partner has agreed to deliver.** That is survivable until a film publishes. It is not survivable after.

---

## The part worth noticing: the free tier is the funnel test

**You do not need links 9 or 10 to prove links 3 through 8 work.**

`visa.html` now sells nothing at the top of the page. It offers to work out your dates and write them down, for free, and says plainly that most people should use the Bureau's portal and keep the PHP 2,500. **That free offer is a complete loop that needs no payment provider, no partner and no price decision.**

Film goes out, viewer lands, viewer emails, you reply the same day with their real dates, viewer now trusts you. **Every link except 7 is already standing for that loop.**

So the order is not "build the whole funnel." It is:

1. **Create the alias.** Link 7 closes. The free loop works end to end
2. **Publish one Madrid film.** Links 0 and 1 close with a phone and no budget. `briefs/00` already specifies three
3. **Watch what arrives.** If nobody emails about their dates when the thing is free, the paid products are not the problem and the films are
4. **Then** the payment rail and the partners, for the people who ask

## A dated thing that argues for publishing now rather than in January

`PLAYBOOK.md` records that YouTube's monetization bar is 1,000 subscribers plus 4,000 watch hours until **1 February 2027**, and 8,000 watch hours for new applicants after that, with channels already in the programme grandfathered.

**You land in January 2027.** Starting the channel then means starting from zero against the higher bar. **You will almost certainly miss the grandfather date either way** with no films published today, so do not treat this as a race you can win. But it does remove the last argument for waiting: **there is no advantage left in holding the channel back, and the Madrid films exist precisely to start the clock early.**

---

## Test it yourself in ten minutes

Do this on your phone, not a laptop, because that is what a viewer uses.

| # | Do | Pass looks like |
|---|---|---|
| 1 | Type `vayanews.com/visa` from memory, no copy and paste | Page loads, no 404 |
| 2 | Read the first screen without scrolling | You can tell what Vaya does and what it costs |
| 3 | Find the free option | The Bureau's portal is named in the first paragraph |
| 4 | Tap the red button | Your mail app opens with the subject already saying `Visa Desk EP02` |
| 5 | Send it to yourself with a passport photo attached | **It arrives. Today it will bounce** |
| 6 | Reply to it as if you were the customer | You can answer with real dates in under five minutes |
| 7 | Now ask: how would I pay this person | **No answer exists on the site** |

**Steps 5 and 7 are the two cuts.** Step 5 is five minutes of your time. Step 7 is one decision.

---

## What is deliberately not in this funnel

- **No analytics, no cookies, no pixel.** The email subject line is the attribution: one film points at one page, and that page's button carries the code. **You count inbound emails by code.** It is manual and it is enough below a hundred a month, and it keeps `privacy.html` true, which is worth more than a dashboard
- **No signup wall on the free guide.** `starter-kit.html` asks for nothing. That is a decision already in `DECISIONS.md`: Vaya does not sell information
- **No `?ep=` parameter yet.** `kit/README.md` specifies `vayanews.com/manila?ep=01`. It only earns its keep when two films point at one page, and today each film points at its own. **Add it when the flagship and a product film both send people to the same place**

## Accept when

A stranger can watch a film, retype the URL from memory, land on a page whose episode code matches what they just saw, click once, reach a human the same day, and be told how to pay. **Six of those seven are true today. The sixth is an alias and the seventh is a decision.**
