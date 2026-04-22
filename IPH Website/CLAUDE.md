# Innovative Projects Hub — Website

Single-page marketing website for a social media management agency targeting small businesses.

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
| `owner-photo.png` | Owner's professional headshot (used in "Who This Is For" section) |
| `office-photo.jpg` | Office workspace photo (saved for future use, not currently displayed) |
| `assets/logo-drafts/` | Logo design exploration files (2 rounds of drafts) |
| `playground/CLAUDE.md` | Original project docs (outdated, replaced by this file) |
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
- **Gradient text:** `.gradient-text` class — accent to plum gradient on text

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
- **Logo drafts saved in:** `assets/logo-drafts/`

## Page Sections (in order)

1. **Navigation** — fixed top, glassmorphism backdrop blur, monogram crest logo + links + "Book a Call" CTA, mobile hamburger menu
2. **Hero** — full viewport, gradient blobs (parallax on desktop), headline + subtitle + 2 CTAs, animated workspace mockup (laptop + phone + coffee cup + decorative elements), floating label cards (Engagement, New Followers, Brand Awareness)
3. **Marquee Ticker** — infinite scrolling service keywords
4. **What We Do** (#services) — 4 service cards (Content Planning, Content Creation, Scheduling, Growth Strategy) with numbered icons
5. **Who This Is For** (#who) — checklist layout (Small Business Owners, Service Providers, Busy Entrepreneurs, Overwhelmed by Social Media) + owner photo (portrait, 3:4 aspect ratio)
6. **Pricing** (#pricing) — 3-tier cards (Foundation, Growth "Most Popular", Visibility+Growth). All show "Custom Pricing" with "Book a call to discuss". Buttons say "Book a Call"
7. **How It Works** (#how-it-works) — 4 numbered steps with arrow connectors (Consultation, Strategy, Content Creation, Scheduling + Growth)
8. **Why Choose Us** (#why) — 4 value props with icons (Done-for-You, Strategy + Execution, Built for Small Businesses, Focused on Real Growth)
9. **Results** (#results) — 4 outcome cards (Stronger Online Presence, More Engagement, Consistent Branding, More Customer Inquiries)
10. **Final CTA** — centered call-to-action with booking button + email contact line
11. **Footer** — monogram crest logo, nav links, email contact, copyright 2026

## Hero Workspace Mockup

The hero visual is a CSS-only animated illustration (no images). Elements:

- **Laptop** with dark screen showing a social media dashboard (sidebar + 4 colorful post cards in gold/plum/sage gradients)
- **Phone** floating to the right with a post preview and a pulsing gold notification badge
- **Coffee cup** with animated rising steam
- **Decorative elements:** spinning circles (gold + plum), bobbing sage circle, twinkling dot grid in brand colors, rotating plus signs, pulsing diamond
- **Glow effect:** radial gradient behind laptop
- **Animations:** laptop floats (6s), phone floats (5s), screen shimmer sweep (4s), post cards glow sequentially (4s staggered), sidebar lines pulse (3s), steam rises (2.5s), circles spin/bob, dots twinkle, plus signs rotate, badge pulses

## Integrations

### Google Calendar Booking
- **Link:** https://calendar.app.google/ptUn1uAM312FhpsL9
- **All booking buttons** across the site open this link in a new tab
- **Buttons that link here:** Nav CTA, mobile menu, hero button, 3 pricing card buttons, final CTA button, footer contact link

### Email Contact
- **Address:** iph.growthofficer@gmail.com
- **Displayed in:** Final CTA section and footer
- **Uses `mailto:` links** so clicking opens the user's email client

## Animations & Interactions

- **Scroll animations:** `.fade-up`, `.slide-left`, `.slide-right` — triggered via IntersectionObserver at 8% threshold
- **Stagger effect:** children inside `.stagger` containers get sequential 0.12s delays
- **Parallax blobs:** 3 gradient blobs in hero move on scroll (desktop only)
- **Navbar:** adds `.scrolled` class with box-shadow after 20px scroll
- **Buttons:** translateY(-3px) on hover with shadow transitions
- **Marquee:** CSS `@keyframes marquee-scroll` infinite loop
- **Workspace mockup:** multiple layered CSS animations (see Hero Workspace Mockup section)

## Responsive Breakpoints

- **768px:** single-column layouts, hero visual reorders above text, mobile menu activates, floating cards hidden, mockup scales down to 300px max
- **480px:** full-width buttons, stacked CTA buttons

## Removed Sections

- **Stats Bar** (removed March 2026) — was between What We Do and Who This Is For (150+ Posts Published, 95% Client Retention, 3x Engagement Lift, 24/7 Content Support). Removed as placeholder data.
- **Hero floating stat numbers** (removed March 2026) — cards showed +147%, +2.4K, 3x Faster. Numbers removed to avoid misleading claims. Cards now show labels only (Engagement, New Followers, Brand Awareness).
- **Dollar pricing** (removed March 2026) — Foundation $497-697, Growth $997-1497, Visibility+Growth $1997-2997. Replaced with "Custom Pricing" / "Book a call to discuss" while pricing is being finalized.
- **Hero lifestyle photo** (removed March 2026) — office photo (`office-photo.jpg`) was tested but didn't match site aesthetic. Replaced with CSS workspace mockup illustration.

## Placeholders / TODOs

- No favicon or Open Graph meta tags
- No analytics or tracking scripts
- Hero lifestyle photo area uses mockup illustration (could swap for a real photo later)
- `office-photo.jpg` saved in project but not displayed (available for future use)
- Custom domain not yet configured (currently using GitHub Pages URL)

## Deployment

To update the live site:
1. Edit files locally (through Claude Code or any editor)
2. Open **GitHub Desktop** — it will show the changes
3. Write a summary and click **Commit to main**
4. Click **Push origin**
5. Site updates in 1-2 minutes at the live URL

## Conventions

- All CSS is in a single `<style>` tag in `<head>`
- All JS is in a single `<script>` tag before `</body>`
- Sections use semantic HTML (`<section>`, `<nav>`, `<footer>`)
- Icons are inline SVGs (no icon library)
- CSS uses custom properties extensively for theming
- Animations use CSS transitions + JS IntersectionObserver (no animation library)
- Mobile menu uses `.open` class toggle
- All external links open in new tabs (`target="_blank"`)
