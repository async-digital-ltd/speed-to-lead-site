# speed-to-lead-site

Web home for Speed to Lead, hosted at [speed-to-lead.async-digital.com](https://speed-to-lead.async-digital.com) via GitHub Pages.

## Why a separate repo

Same pattern as `audient-site` and `demo-site`. Speed to Lead has its own subdomain so the bare domain (`async-digital.com`) keeps doing whatever Async Digital wants it to do (currently a brief Speed to Lead teaser on the homepage), and Helen has a clean URL to share with prospects.

## Structure

- `index.html` — landing page (English)
- `index.cy.html` — landing page (Welsh) (TODO)
- `assets/` — favicon and logo files; brand tokens are loaded cross-domain
- `BRAND.md` — defers to the canonical Async Digital brand foundation
- `CNAME` — custom domain config for GitHub Pages

## Shared brand assets

Brand tokens (`brand.css`) and runtime constants (`brand.js`) are loaded from `https://async-digital.com/assets/...` via absolute URL. Single source of truth lives in [`async-digital-site`](https://github.com/async-digital-ltd/async-digital-site). No duplication, but the cross-domain coupling means a `BRAND.*` change in the parent repo ripples here through the cache-bust.

## Brand and voice

[`BRAND.md`](./BRAND.md) is the index. Voice rules and positioning are inherited from the parent repo unchanged. If you're editing copy here, run the `marketing-auditor` agent before publishing.

## Pre-launch follow-ups

- Welsh mirror at `index.cy.html`
- Real Cal.com URL on every `#book` link (currently anchor-scrolls to the final CTA)
- `https://async-digital.com/privacy/speed-to-lead.html` page (referenced by the footer; lives in the parent repo under the compliance lane)
- DNS / Cloudflare Pages custom-domain wiring at `speed-to-lead.async-digital.com`
- Helen's actual average new-patient value baked into the calculator default (currently £450 placeholder)
