# Signal Electric LLC — Project Instructions

Use these instructions for every change to this site. This is a standalone project. Do not mix it with any other site.

## Purpose

One-page business-card website for **Signal Electric LLC**, a licensed electrical contractor in Signal Mountain / Chattanooga, TN.

The page should stay simple: company identity, phones, services, trust copy, reviews, and a way to call or email. It is not a multi-page app, blog, store, or booking system unless the user explicitly asks for that later.

## Hard boundaries

- **Do not touch the knitting website** or any other repository.
- Work only in GitHub repo `erichawks/signal-electric-llc`.
- Keep the site a **static single-page** site. Primary file: `index.html`.
- Do not add React, Next.js, Supabase, or a build step unless the user asks.
- Do not invent services, ratings, licenses, names, or phone numbers.
- Prefer small visual edits over rewriting copy. If the user asks to change one thing, change only that thing.
- When the user rejects a visual change (for example service photos), do not bring it back later.

## Repos and URLs

| Item | Value |
|---|---|
| GitHub | https://github.com/erichawks/signal-electric-llc |
| Live site | https://signal-electric-llc-eric-f564.vercel.app |
| Vercel project | `signal-electric-llc` (personal account `eric-f564`) |
| Old / existing domain | https://www.signal-electric.com/ (Squarespace; source for colors and company facts) |
| Facebook | https://www.facebook.com/p/Signal-Electric-LLC-61556335614519/ |

After editing `index.html`, **commit to GitHub and deploy to Vercel production**. GitHub push does not always update the live alias. Use the Vercel deploy tool with the current `index.html` when needed.

Vercel Deployment Protection / SSO can block anonymous visitors, crawlers, and PDF print. If a fetch returns a Vercel login page, use the local/GitHub HTML instead of the live URL.

## Company facts (canonical)

Use these exactly unless the user corrects them:

- Business: Signal Electric LLC
- Location: Signal Mountain, TN 37377
- Service area: Signal Mountain and the greater Chattanooga area
- People: Calob Merryfield `(423) 285-8008`; Benjamin Bleasdale `(931) 256-6229`
- Email: Info@signal-electric.com (`mailto:info@signal-electric.com`)
- TN Electrical License **#80668**
- Tesla Certified Installer (do not display as a hero badge unless asked)
- Work: residential and commercial — service calls, EV chargers, standby generators, panels/upgrades, lighting/receptacles, new construction and remodels
- Logo: official mark from the existing site / Facebook, currently  
  `https://images.squarespace-cdn.com/content/v1/65a00dbad08a6229f37c8c6e/284bb9d6-bfa2-41c8-a791-a0bf3ee6ded9/IMG_0002.png?format=750w`

Do not confuse this company with other “Signal Electric” businesses.

## Design system

Colors come from the logo and the old Squarespace site. Light page background so the white field in the logo blends.

| Token | Hex | Use |
|---|---|---|
| Background | `#f4f1ea` | Page and header wash |
| Surface | `#ffffff` | Cards |
| Navy | `#24363a` | Headlines, logo wordmark |
| Ink | `#1b2438` | Body |
| Muted | `#5d6a73` | Supporting text |
| Rust | `#d0573a` | Accent, buttons, “service.”, rust rules |
| Sage | `#6f8b7d` | Header city line and license line |

Fonts:

- Headlines / wordmark: **Oswald**
- Body: **Inter**

Layout:

- Sticky header, max content width ~1120px
- Header logo **156px** tall desktop, **108px** mobile
- Wordmark beside logo, stacked and centered:
  - Line 1: `Signal Electric LLC` (Oswald, navy, uppercase)
  - Line 2: `Signal Mountain, TN` (sage, small caps, rust bars on both sides)
- Header right: **TN License #80668** only — same type style as the city line. No header call buttons.
- Hero left: eyebrow, headline, lede. **No** Call/Text/Facebook buttons and **no** badge pills under the headline.
- Hero right: “Need an electrician?” call box
- Services grid (3 columns desktop, 1 column mobile)
- About split: NEC / service area
- Reviews
- Rust CTA band with the two phone numbers
- Slim footer

Headline must stay:

```
Honest, reliable,
consistent service.
```

“service.” is rust. Keep extra space between the two lines so the comma after RELIABLE does not touch CONSISTENT. Use two block lines (`.h1-line`) with a small top margin on the second line.

## Call box and footer (current)

Call box rows:

1. Calob Merryfield — (423) 285-8008 — `tel:+14232858008`
2. Benjamin Bleasdale — (931) 256-6229 — `tel:+19312566229`
3. Email — Info@signal-electric.com — `mailto:info@signal-electric.com`

Do not repeat owner/address/email under the call box.

Footer:

- Left: `TN Electrical License #80668` and **Join us on Facebook** with the blue Facebook icon SVG
- Right: service-area line and copyright
- Do **not** put company name + city + both phone numbers in the footer again

## Reviews

Left quote stays the Calob and Ben “master electricians” review.

Right quote is the Tesla charger review, **not** a lamp / light-fixture review:

> “Five stars. Signal Electric was fantastic! They were polite, courteous, and installed our Tesla charger perfectly. I will use them again for sure!”

## What not to add unless asked

- Photos inside the service cards (tried and removed)
- Extra logos above “Need an electrician?”
- Header phone / Call or Text buttons
- Hero badge row (Licensed, Tesla, BBB, etc.)
- FAQ block or SEO-rewritten visible headlines such as “Licensed electrician in Signal Mountain, TN”
- Combining this repo with the knitting project

Technical SEO files (`robots.txt`, `sitemap.xml`, `vercel.json`, title/meta description) may exist. Do not change visible page copy just to “do SEO.” If asked for SEO, keep the current wording and work in head tags / structured data / crawl files.

## How to make a change

1. Read current `index.html` from GitHub (`main`) and use its blob SHA when updating.
2. Change only what the user asked for.
3. Commit a short message on `main`.
4. Deploy the same `index.html` to Vercel project `signal-electric-llc`, target `production`.
5. Tell the user to hard-refresh https://signal-electric-llc-eric-f564.vercel.app

## Files in the repo

- `index.html` — the site
- `robots.txt`, `sitemap.xml`, `vercel.json` — hosting / crawl helpers
- `PROJECT_INSTRUCTIONS.md` — this document
- `README.md` — short human overview
