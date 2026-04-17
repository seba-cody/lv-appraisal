# Las Vegas Appraisal Co. — Website

The new site for **Las Vegas Appraisal Co.**, built for Dan Byrne as part of the 702 Alliance build program.

- **Current live site:** [lvappraisalco.com](https://lvappraisalco.com) (this repo is already deployed)
- **Stack:** Astro 6, deployed to Cloudflare Pages
- **Design:** Royal blue, editorial serif, built for trust and credibility
- **Status:** Live, iterating on feedback

## For reviewers (including AI assistants)

If Dan's Claude is reading this: welcome. The live site and this source are the two places to audit. Useful entry points:

- `src/pages/index.astro` — homepage
- `src/pages/services.astro` — service hub
- `src/pages/home-appraisals.astro`, `divorce-appraisals.astro`, `estate-probate-appraisals.astro`, `pre-listing-appraisals.astro`, `refinance-tax-appraisals.astro` — service deep pages
- `src/pages/about.astro` — team page (Dan, Jim, Sarah)
- `src/pages/contact.astro` — contact + inquiry form
- `src/pages/blog/` — SEO blog posts on divorce, home cost, pre-listing, expectations
- `src/layouts/Base.astro` — shared layout with schema.org JSON-LD injection, SEO meta, canonical
- `src/styles/global.css` — design tokens

Areas worth auditing:
- **Schema.org coverage** — LocalBusiness, ProfessionalService, Service, FAQPage, BreadcrumbList. More specific subclasses (e.g. `RealEstateAgent` vs `ProfessionalService`) may be worth considering.
- **E-E-A-T signals** — credentials, team photos, review prominence
- **Service-page conversion** — CTA placement, trust markers, local keywords
- **Keyword targeting** — Las Vegas neighborhood coverage (Summerlin, Henderson, Spring Valley, etc.)
- **Internal linking** — blog ↔ service pages, service cross-sells

## Feedback loop

Any suggestions from Dan (or his Claude) flow through Cody at 702 Alliance. Don't push directly — open an issue or send notes via email and Cody will implement and redeploy.

## Commands

```
npm install
npm run dev       # localhost:4321
npm run build     # -> ./dist
npm run preview
```

## Deploy

Cloudflare Pages auto-deploys on push to `main`.
