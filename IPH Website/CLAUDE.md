# Innovative Projects Hub — Website

Single-page marketing website positioning Gina as an AI automation & implementation specialist for small businesses. Target audience: non-technical small business owners (real estate agents, salons, tire shops, home remodeling, HVAC) who want AI working for them without learning it themselves.

**Live URL:** https://iphgrowthofficer-star.github.io/innovative-projects-hub/
**Repository:** https://github.com/iphgrowthofficer-star/innovative-projects-hub
**Hosting:** GitHub Pages (free), deployed from `main` branch

## Tech Stack

- **Single file:** `index.html` (all HTML, CSS, and JS embedded)
- **No build tools, frameworks, or dependencies**
- **Fonts:** Google Fonts — Playfair Display (serif headings) + Inter (sans-serif body) + Cormorant Garamond (logo text)

## Project Structure

| File/Folder | Purpose |
|-------------|---------|
| `index.html` | The entire site (HTML + embedded CSS + JS) |
| `owner-photo.png` | Owner's professional headshot (used in "Meet Your Strategist" section) |
| `office-photo.jpg` | Office workspace photo (saved for future use, not currently displayed) |
| `assets/logo-drafts/` | Logo design exploration files (2 rounds of drafts) |
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

- `--max-width: 1200px` — container max width
- `--section-pad: clamp(100px, 12vw, 160px)` — vertical section padding
- Container horizontal padding: 24px

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

## Page Sections (in order)

1. **Navigation** — fixed top, glassmorphism backdrop blur, monogram crest logo + links + "Book a Call" CTA, mobile hamburger menu
2. **Hero** — full viewport, gradient blobs, H1 "AI Automation & Implementation for Small Businesses", subtitle with punchy "40 hours" hook, 2 CTAs, animated workspace mockup, floating label cards (Hours Saved, AI Agents Active, Workflows Automated)
3. **Marquee Ticker** — infinite scrolling: Workflow Automation, AI Agent Implementation, Process Design, System Integration, AI Strategy, Operations Automation, Custom AI Builds, 24/7 AI Operations
4. **Industries We Serve** — 5 cards: Real Estate, Salons & Spas, Tire & Auto Shops, Home Remodeling, HVAC Services. Copy says "ready to build for" (honest — Gina has no existing clients yet)
5. **What We Do** (#services) — 4 service cards: AI Workflow Design, Agent Implementation, Process Automation, Marketing Strategy & Online Presence
6. **Meet Your Strategist** (#about) — Gina's photo + bio + 4 strength items (20+ Years Business Growth, Custom AI Solutions, Hands-Off AI Management, Ongoing Support)
7. **Who This Is For** (#who) — 4 items targeting non-tech small business owners worried about competitive edge
8. **Pricing** (#pricing) — 3-tier cards (AI Assistant Team, AI Operations Team "Most Popular", Full AI Business Team). All "Custom Pricing / Book a call to discuss"
9. **How It Works** (#how-it-works) — 3 steps: Discovery Call, AI Implementation, You Scale
10. **Why Choose Us** (#why) — 4 value props: Custom-Built Teams, Strategy + Execution, No Tech Expertise Required, Measurable Time Savings
11. **Results** (#results) — 4 outcome cards: 40 Hours Saved Monthly, Consistent Execution, Personalized Automation, Scalable Operations
12. **Final CTA** — "Stop doing the work AI can handle" + booking button + email
13. **Footer** — monogram crest logo, nav links, email contact, copyright 2026

## SEO (added April 2026)

- **Title:** "Innovative Projects Hub — AI Automation & Implementation for Small Businesses"
- **Meta description:** "We build custom AI agent teams for small businesses. Automate customer follow-ups, marketing, and daily operations so you can focus on growth."
- **Open Graph tags:** og:title, og:description, og:image (owner-photo.png), og:url
- **Twitter Card tags:** summary_large_image
- **Canonical URL:** set to GitHub Pages URL
- **Favicon:** inline SVG (no file needed)
- **H1:** keyword-rich — "AI Automation & Implementation for Small Businesses"

## Integrations

### Google Calendar Booking
- **Link:** https://calendar.app.google/ptUn1uAM312FhpsL9
- **All booking buttons** across the site open this link in a new tab

### Email Contact
- **Address:** iph.growthofficer@gmail.com
- **Uses `mailto:` links**

## Animations & Interactions

- **Scroll animations:** `.fade-up`, `.slide-left`, `.slide-right` — triggered via IntersectionObserver at 8% threshold
- **Stagger effect:** children inside `.stagger` containers get sequential 0.12s delays
- **Parallax blobs:** 3 gradient blobs in hero move on scroll (desktop only)
- **Navbar:** adds `.scrolled` class with box-shadow after 20px scroll
- **Marquee:** CSS `@keyframes marquee-scroll` infinite loop
- **Workspace mockup:** multiple layered CSS animations

## Responsive Breakpoints

- **1024px:** industries grid 3 columns, pricing single column
- **768px:** single-column layouts, hero visual reorders above text, mobile menu activates, floating cards hidden, mockup scales down to 300px max
- **480px:** full-width buttons, stacked CTA buttons, industries single column

## Removed / Changed

- **Social media positioning** (April 2026) — site was originally a social media agency; fully pivoted to AI implementation
- **Stat cards** (April 2026) — "6 AI Agents / 48h / 24/7" cards removed from hero (broken HTML, placeholder data)
- **Stats Bar** — removed earlier as placeholder data
- **Dollar pricing** — removed earlier; using "Custom Pricing" while finalizing
- **"Content & Social Media" service** — replaced with "Marketing Strategy & Online Presence"
- **"Four Simple Steps"** — corrected to Three (only 3 steps exist)

## Placeholders / TODOs

- No analytics or tracking scripts yet
- Custom domain not yet configured
- `office-photo.jpg` saved but not displayed (available for future use)
- No schema markup (LocalBusiness/Service) — medium priority SEO improvement

## Deployment

To update the live site:
1. Edit `index.html` locally through Claude Code
2. Open **GitHub Desktop** — it will show the changes
3. Write a summary and click **Commit to main**
4. Click **Push origin**
5. Site updates in 1-2 minutes — hard refresh with `Cmd+Shift+R`

## Copy Conventions

- **Honest positioning:** Gina has no existing clients. Never claim past results. Use forward-looking language ("ready to build for", "we can help").
- **Non-tech audience:** Plain language. No jargon. Frame everything as done-for-you.
- **No em dashes** — use commas, periods, or ellipses
- **40 hours** — consistent phrasing throughout (not "20-40 hours")

## Code Conventions

- All CSS in a single `<style>` tag in `<head>`
- All JS in a single `<script>` tag before `</body>`
- Sections use semantic HTML (`<section>`, `<nav>`, `<footer>`)
- Icons are inline SVGs (no icon library)
- CSS uses custom properties extensively for theming
- Mobile menu uses `.open` class toggle
- All external links open in new tabs (`target="_blank"`)
