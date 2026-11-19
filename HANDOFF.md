# IPH Website Handoff

Last updated: 2026-11-18

## Current Status

- Current live site: https://iphgrowthofficer-star.github.io/innovative-projects-hub/.
- Published baseline: `503816c` (`Redesign IPH for small business AI services`).
- Custom domain selected and registered through Namecheap: `innovativeprojectshub.com`.
- Custom-domain configuration is prepared on branch `custom-domain-setup`; it is not deployed yet.
- Namecheap account owns the domain, but it currently uses PremiumDNS (`pdns1.registrar-servers.com`, `pdns2.registrar-servers.com`). Direct Advanced DNS returned a Namecheap server error. A bulk Host Records submission returned to the domain list, but direct queries to both authoritative servers still show no apex A or `www` CNAME records.
- Do not merge/publish the custom-domain branch until the DNS records are visible on the active authoritative nameservers and the domain resolves.
- The site is static HTML/CSS/JavaScript with no build system or package dependencies.

## Project Files

- `index.html`: Home page and brand styles.
- `assets/site.css`: shared responsive design for dedicated pages.
- `assets/site.js`: mobile menu behavior.
- `owner-photo.png`: founder portrait.
- `resources/small-business-ai-opportunity-checklist.txt`: downloadable resource.
- `robots.txt` and `sitemap.xml`: crawl instructions and current routes.
- `IPH Website/CLAUDE.md`: project conventions and design notes.
- `HANDOFF.md`: this resume note.

## Business Positioning

IPH provides platform-independent AI training, consulting, and implementation, primarily for small business owners and entrepreneurs. Professionals, startups, service and retail businesses, busy moms, and individuals are also included. Claude is a featured training option, but the brand is not Claude-only. Avoid exaggerated claims, invented outcomes, client names, credentials, or testimonials.

## Pages

Each page is a real directory route with its own `index.html`:

- `/` Home
- `/services/`
- `/claude-training/`
- `/ai-automation/`
- `/ai-consulting/`
- `/custom-ai-agents/`
- `/training/`
- `/courses/`
- `/who-we-help/`
- `/about/`
- `/ai-training-chicago/`
- `/resources/`
- `/blog/` with article outlines and a reusable article template, not pretend-finished posts
- `/faq/`
- `/contact/`
- `/privacy-policy/`
- `/terms-of-service/`
- `/404.html`

The About navigation link on Home anchors to Gina's founder section; the dedicated `/about/` page is also available.

## Offers and Integrations

- The existing Claude Starter Session is $150 for one hour and retains its current deliverables.
- The existing three-session package is $399.
- The existing Agent Build Consultation is $200/hour with a two-hour minimum. This is a consultation/planning offer; integrations, deployment, testing, and maintenance are not automatically included.
- Course outlines remain Claude for Small Business and Claude for Moms. The existing $47–$97 range is described as a launch range for courses in development; confirm before enrollment.
- Booking uses the existing Google Calendar URL: `https://calendar.app.google/ptUn1uAM312FhpsL9`.
- Courses embed the existing Google Form: `https://forms.gle/FWXBfhTTXi2qDUtn6`. It asks course interest, name, and email.
- No other email signup form or analytics ID is fabricated.
- Contact email already used by IPH: `iph.growthofficer@gmail.com`.

## Completed Locally

- Platform-independent AI positioning and a rebuilt Home flow.
- Benefit cards, audience cards, service previews, founder credibility, three-step process, featured offers, differentiators instead of testimonials, real downloadable checklist, FAQ, and booking CTAs.
- Dedicated pages for services, training, audiences, Chicago, resources, blog outlines, contact, FAQ, and policies.
- Unique page titles/descriptions, canonicals, sitemap, robots, Organization/Person/WebSite and relevant Service/FAQ structured data.
- Policy pages explicitly request owner/legal review; no physical office address or analytics IDs are invented.

## Owner Inputs / Follow-Ups

- Configure the GitHub Pages records in the active PremiumDNS zone, or intentionally switch to Namecheap BasicDNS only after checking whether PremiumDNS or other DNS/email services must be retained. Do not change nameservers blindly.
- Required apex records: four A records for host `@` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`.
- Required `www` record: CNAME host `www`, target `iphgrowthofficer-star.github.io`.
- Preserve existing email-related DNS records and do not alter DNSSEC unless specifically troubleshooting it.
- After DNS resolves to GitHub Pages, publish branch `custom-domain-setup` to `main`, confirm the custom domain in GitHub repository Settings > Pages, enable Enforce HTTPS when GitHub offers it, and verify both apex and `www` behavior.
- DNS currently points to Namecheap parking (`@` A record `162.255.119.8`; `www` CNAME `parkingpage.namecheap.com.`), so the custom domain is not live yet.
- Confirm the Google Calendar event type and availability.
- Confirm Google Form responses remain enabled and arrive as expected.
- Have a qualified professional review the privacy and terms drafts before treating them as final policies.
- Provide GA4, Google Search Console, and Bing Webmaster IDs or access if analytics and webmaster setup should be completed.
- For local SEO, verify or create Google Business Profile and Bing Places only if eligible; keep business details consistent, consider suitable local directories and LinkedIn presence, and request only genuine customer reviews.
- The site does not claim a public office address. Confirm location details before adding any address or map.
- Consider local networking with Chicago small-business groups after confirming the service area and meeting arrangements.
- Confirm whether group training will be offered and approve any future pricing before publication.
- Do not add testimonials unless genuine and authorized.

## Local Preview

From the repository folder run:

```sh
python3 -m http.server 8000
```

Open http://localhost:8000. The Python command is only for local static preview; no dependencies/build step are needed.

## Resume and Publish

```sh
cd "/Users/growthofficer/Learning/IPH Start up/innovative-projects-hub"
git status --short --branch
```

Validate internal paths, mobile navigation, meta tags, and `git diff --check`. Update `IPH Website/CLAUDE.md` and this handoff if structure or status changes. Custom-domain setup is pending the owner changing Namecheap DNS; after DNS points to GitHub Pages, merge `custom-domain-setup` to `main`, set/verify the domain in GitHub Pages settings, and wait for HTTPS provisioning.