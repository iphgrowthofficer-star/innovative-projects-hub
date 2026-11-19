# Innovative Projects Hub — Website

Static website for Innovative Projects Hub, offering platform-independent AI training, consulting, and implementation for small business owners, entrepreneurs, professionals, and individuals. Claude remains a featured training option, alongside ChatGPT and other tools when appropriate.

**Current live URL:** https://iphgrowthofficer-star.github.io/innovative-projects-hub/
**Custom domain:** innovativeprojectshub.com (registered; DNS and GitHub Pages activation are pending)
**Repository:** https://github.com/iphgrowthofficer-star/innovative-projects-hub
**Hosting:** GitHub Pages (free), deployed from `main` branch

## Tech Stack

- Static HTML pages using directory `index.html` files for clean GitHub Pages URLs.
- Root `index.html` is the homepage; `assets/site.css` and `assets/site.js` are shared by the dedicated pages.
- No build tools, frameworks, or package dependencies.
- Fonts: Google Fonts — Playfair Display, Inter, and Cormorant Garamond.

## Project Structure

| File/Folder | Purpose |
|-------------|---------|
| `index.html` | Homepage, with existing brand styles and home content |
| `assets/site.css` | Shared layout and responsive styles for dedicated pages |
| `assets/site.js` | Shared mobile-menu behavior for dedicated pages |
| `owner-photo.png` | Gina's founder photo, displayed on Home and About |
| `office-photo.jpg` | Office workspace photo (saved for future use, not currently displayed) |
| `assets/logo-drafts/` | Logo design exploration files (2 rounds of drafts) |
| `resources/small-business-ai-opportunity-checklist.txt` | Downloadable business AI opportunity checklist |
| `sitemap.xml`, `robots.txt` | Search crawler discovery files |
| `IPH Website/CLAUDE.md` | This file — current project documentation |

## Design System

### Color Palette (CSS custom properties on `:root`)

| Variable | Value | Usage |
|----------|-------|-------|
| `--accent` | `#C4956A` | Primary gold accent |
| `--accent-light` | `#D4AA82` | Light gold variant |
| `--accent-dark` | `#A87B52` | Dark gold variant |
| `--plum` | `#8B6F8E` | Secondary purple accent |
| `--sage` | `#7A9A7E` | Secondary green accent |
| `--dark` | `#141414` | Headings, dark backgrounds |
| `--charcoal` | `#2C2C2C` | Body text |
| `--off-white` | `#FAF9F7` | Hero background |
| `--cream` | `#F3F0EB` | Section backgrounds |
| `--beige` | `#E4DDD3` | Borders, dividers |
| `--warm-gray` | `#9A9088` | Subtitles, muted text |

### Typography

- **Headings:** `var(--font-serif)` — Playfair Display, 600 weight
- **Body:** `var(--font-sans)` — Inter, 300-600 weight
- **Logo text:** Cormorant Garamond, 400 weight, uppercase, wide letter-spacing
- **Section labels:** 0.72rem, uppercase, letter-spacing 0.2em, gold color
- **Gradient text:** `.gradient-text` class — accent to plum gradient on text. Uses `box-decoration-break: clone` to prevent clipping when text wraps across lines.

### Spacing

- Shared pages use a 1160px maximum content width and responsive section spacing.
- The homepage retains legacy embedded styles for the existing brand and hero effects.

### Buttons

- `.btn-primary` — dark background, gradient hover (accent to plum), glow shadow, pill shape
- `.btn-secondary` — transparent with beige border, accent on hover
- `.btn-glow` — animated pulsing box-shadow

### Logo

- **Style:** Monogram crest — double-ring circle with italic lowercase "iph" in gold (Playfair Display italic)
- **Outer ring:** 0.5px solid gold (`--accent`)
- **Inner ring:** 0.5px solid beige (`--beige`), 4px inset
- **Text beside crest:** "Innovative Projects Hub" stacked, Cormorant Garamond uppercase
- **Used in:** Navigation bar and footer
- **Favicon:** Inline SVG version of the iph monogram (no external file needed)

## Page Structure

Each directory contains a real `index.html`, with page-specific title, description, canonical URL, one H1, internal links, and CTAs:

- `/` Home with AI benefit cards, audiences, service previews, founder story, how-it-works, checklist download, FAQs, and booking CTA.
- `/services/`, `/claude-training/`, `/ai-automation/`, `/ai-consulting/`, `/custom-ai-agents/` service overview and detailed offers.
- `/training/` general AI training and coaching; `/courses/` Claude course outlines and the live waitlist form.
- `/who-we-help/`, `/about/`, `/ai-training-chicago/`, `/faq/`, `/contact/` audience, founder, local, FAQ, and contact pages.
- `/resources/` checklist download; `/blog/` article outlines and reusable editorial guidance, not published articles.
- `/privacy-policy/` and `/terms-of-service/` plain-language drafts marked for owner/legal review.
- `/404.html` not-found fallback.

The About nav points to the founder section on Home; `/about/` is also available as a dedicated founder page.

## SEO

- Each page has a unique SEO title, meta description, and canonical URL.
- Homepage Open Graph and Twitter metadata are configured.
- Primary search themes include AI training for small business, AI consulting in Chicago, small-business AI automation, AI productivity coaching, Claude training, and custom AI agents. Use these naturally, based on the actual page content.
- `sitemap.xml` lists current pages; `robots.txt` allows crawling and points to the sitemap.
- Homepage JSON-LD covers Organization, Person, and WebSite; service and FAQ pages add appropriate schema where content supports it.
- No ratings, reviews, physical office address, or unverified achievements are marked up.
- **Favicon:** inline SVG (no file needed)
- **H1:** "Work Smarter. Save Time. Grow Your Business with AI."

## Integrations

### Booking and Waitlist
- Google Calendar booking link: `https://calendar.app.google/ptUn1uAM312FhpsL9`.
- The Courses page embeds the live Google Form; its short link is `https://forms.gle/FWXBfhTTXi2qDUtn6`.
- The form collects course interest, name, and email. No separate nonfunctional signup form is used.
- Current existing prices: Starter Session $150, 3-Pack $399, Agent Build Consultation $200/hour with a two-hour minimum, courses $47–$97 launching range. Get owner approval before changing prices or describing unpriced offers.

## Interactions

- Dedicated page URLs replace the old hidden hash-route SPA pages.
- Shared mobile navigation is controlled by `assets/site.js`.
- The legacy inline homepage styles remain in `index.html`; new dedicated pages use `assets/site.css`.

## Responsive Breakpoints

- Shared pages: 900px tablet layout, 720px mobile navigation and single-column cards, 420px narrow-phone adjustments.
- Homepage includes its retained responsive styles plus short-viewport header/hero adjustments.

## Content Notes

- IPH offers platform-independent AI training, consulting, and implementation. Do not frame the business as Claude-only.
- Distinguish AI training, agent planning, software building, integrations, and deployment. Do not imply deployment is included unless scoped and approved.
- Do not add past-client names or unsupported testimonials/results.
- Keep copy friendly and clear for non-technical readers.

## Placeholders / TODOs

- Confirm the Google Calendar appointment schedule and availability.
- Confirm the embedded Google Form accepts responses and records them as expected.
- Get owner/legal review of Privacy and Terms drafts.
- Add GA4, Search Console, and Bing Webmaster verification only after the owner supplies IDs/access. No IDs are fabricated or embedded.
- No testimonials are published; only add genuine authorized testimonials.
- Local SEO owner tasks: verify/complete Google Business Profile and Bing Places if eligible, keep business details consistent, consider relevant local directories and LinkedIn presence, and request reviews only from real customers without incentives or fabricated claims.

## Deployment

To preview locally, run `python3 -m http.server 8000` from the repository folder and visit `http://localhost:8000`. Static directory pages resolve at paths such as `/services/` and `/ai-training-chicago/`.

GitHub Pages serves the root `index.html` and directory pages from `main`. The custom domain setup is on branch `custom-domain-setup`. Configure Namecheap apex A records to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`; set `www` CNAME to `iphgrowthofficer-star.github.io`; remove conflicting parking records. After DNS resolves, merge the setup branch, confirm the domain under GitHub repository Settings > Pages, and enable HTTPS when available.

## Copy Conventions

- **Honest positioning:** Do not imply past clients, testimonials, or outcomes that are not established.
- **Non-technical audience:** Plain, friendly language. Explain unfamiliar terms.
- **No em dashes** — use commas, periods, or ellipses

## Code Conventions

- Dedicated pages use semantic HTML and shared styles/scripts from `assets/`.
- Maintain existing brand colors and typography; keep layouts mobile-responsive.
- Do not add unnecessary dependencies or expose secrets in frontend code.
- External links that open in new tabs use `rel="noopener"`.
