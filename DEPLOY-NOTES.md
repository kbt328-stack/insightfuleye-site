# Deploy Notes — insightfuleye.com

7 static HTML pages + styles.css. No build step, no framework — every page is real server-rendered HTML, exactly what the Client Zero audit prescribed. Host anywhere (Vercel, Netlify, Cloudflare Pages, or any static host).

## Before launch
1. **Contact form (hub-and-spoke):** in `contact.html`, replace the dashed `.form-slot` box with your GHL form embed iframe. The slot is marked with a big comment block including the exact embed format.
2. **Founder Package link:** in `index.html`, the Founder Package callout button currently points to `contact.html`. Update the `<!-- TODO -->` marked href to your GHL funnel subdomain (e.g. `go.insightfuleye.com/founder-package`) once you've moved the funnel off the root domain.
3. **Client Zero PDF:** in `case-studies.html`, there's a TODO to link the lightly-redacted audit PDF once you publish it.
4. **DNS:** point the root domain at this site's host. Move the GHL portal/funnel to a subdomain (e.g. `app.` or `go.`). The root must serve this site — that's the #1 audit fix (T-01).

## What's already done per the audit
- Category + geography ("AI marketing agency in Rhode Island") in the first 100 words of the homepage
- Full head metadata on every page: unique title, description, canonical, OG/Twitter cards
- JSON-LD: Organization + LocalBusiness + WebSite on the homepage; Service + FAQPage schema on all three service pages; Person/AboutPage on About; entity story resolving the photography history
- Iris demo callout on the homepage, voice-agent page, and contact page
- robots.txt + sitemap.xml (submit the sitemap in Google Search Console after launch)
- Hub-and-spoke internal linking: home → 3 service spokes → audit CTA on every page

## After launch (per the audit scoreboard)
- Submit sitemap in Search Console; request indexing on all 7 pages
- July 1: first scoreboard run against the Client Zero baselines
- Phase 2: legacy photography listings sweep + GBP for the agency itself
