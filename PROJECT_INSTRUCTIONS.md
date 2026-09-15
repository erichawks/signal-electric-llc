# One-Page Business Site — Project Template

Use this as the Grok project instructions for a simple local-business landing page. Fill the placeholders in **Site instance** once per client, then follow the rest as-is.

Do not hard-code a client name, GitHub repo, or Vercel project into the standing rules. Read those from **Site instance** (or ask if it is blank).

---

## Site instance

Copy this block into the project and fill it in before the first build. Leave unused lines blank.

```
Business name:
Legal name (if different):
City / state / ZIP:
Service area:
Owner / contacts (name + phone or email):
License / insurance / certifications:
Primary email:
Facebook / other social URLs:
Logo URL or file:
Existing site or brand references:
Headline:
GitHub owner/repo:
Vercel project name:
Live URL:
Custom domain:
Out of scope repos (never touch):
Rejected ideas (do not bring back):
```

---

## Purpose

Build and maintain a **one-page business-card website**: identity, how to reach the business, what they do, a little trust copy, and a clear call to action.

It is not a multi-page app, blog, store, membership site, or booking system unless the user explicitly asks for that later.

---

## Hard boundaries

- This project is **standalone**. Never combine it with, or edit, any repo listed under “Out of scope repos.”
- Create a **new** GitHub repository and a **new** Vercel project for each client. Do not reuse another client’s repo or deployment.
- Keep the site **static**. Primary file is `index.html` (plus optional `robots.txt`, `sitemap.xml`, `vercel.json`).
- Do not add React, Next.js, a CMS, or a database unless the user asks.
- Do not invent services, ratings, licenses, reviews, names, or phone numbers. If a fact is missing, ask.
- Prefer the smallest change that matches the request. Do not restyle the whole page to fix one line.
- If the user rejects a visual or copy change, record it under “Rejected ideas” and do not reintroduce it.

---

## Stack and shipping

Default stack:

- One `index.html` with embedded CSS
- Optional crawl files: `robots.txt`, `sitemap.xml`
- Optional `vercel.json` for static headers
- GitHub for source
- Vercel for hosting

Workflow for every visible change:

1. Read the current `index.html` from the instance GitHub repo (`main`) and use its blob SHA when updating.
2. Change only what was asked.
3. Commit a short message on `main`.
4. Deploy that same `index.html` to the instance Vercel project, **production**.
5. Tell the user to hard-refresh the live URL.

A GitHub commit does not always update the live alias. Deploy to Vercel explicitly when the live site must match.

If a live URL returns a host login wall (deployment protection / SSO), do not treat that page as the site. Use the GitHub HTML instead for screenshots, PDFs, and verification.

---

## Page recipe

Keep this structure unless the user asks to change it:

1. **Header** — logo + two-line wordmark + one quiet trust line (license, city, or similar). No header call buttons unless requested.
2. **Hero** — short eyebrow, headline, one lede paragraph. Contact card on the side for phones / email.
3. **Services** — small grid of offerings. Icons or short text only unless photos are requested and kept.
4. **Trust / area** — credentials, service area, guarantee.
5. **Reviews** — only real quotes the user provides or approves.
6. **CTA band** — phones or email.
7. **Footer** — license or legal line, one social link, copyright. Do not dump the full contact block again if it already lives in the call card.

Mobile: single column, readable tap targets, logo scaled down.

---

## Design rules

- Pull colors from the **logo** and any **existing site**. Use a light page background if the logo has a light field so the mark blends.
- Two typefaces is enough: one condensed/display face for headlines and wordmark, one sans for body.
- Wordmark: business name on the first line, city/state (or tagline) centered under it.
- Keep headline line-height loose enough that commas and descenders do not collide with the next line.
- Do not add decorative stock photos unless the user asks. If they later say remove them, remove them.
- Do not sprinkle keyword-stuffed headlines over a layout the user already approved. If they want SEO, keep visible wording and work in title/meta, schema, `robots.txt`, and `sitemap.xml`.

---

## Content rules

- Use official names, numbers, and URLs from **Site instance**.
- Put `tel:` and `mailto:` links on every phone and email.
- Social links open in a new tab and use a recognizable icon plus a short label (for example “Join us on Facebook”).
- Do not change the subject of a customer quote unless the user says to.
- Distinguish this business from similarly named companies.

---

## New client checklist

1. Fill **Site instance**.
2. Confirm this is a new repo and new Vercel project.
3. Collect logo, colors, phones, email, license, and any quotes.
4. Build the one-pager from the recipe above.
5. Ship GitHub + Vercel.
6. Stop. Wait for visual notes. Iterate in small passes.

---

## Standard files

| File | Role |
|---|---|
| `index.html` | The site |
| `robots.txt` | Crawl allow |
| `sitemap.xml` | Live URL only, once known |
| `vercel.json` | Static hosting headers |
| `PROJECT_INSTRUCTIONS.md` | This template |
| `README.md` | Short human overview for the repo |

When starting a new client from this template, copy these instructions into that project unchanged, then fill **Site instance** only.
