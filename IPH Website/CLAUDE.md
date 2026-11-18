# Innovative Projects Hub — Website

Static website for Innovative Projects Hub, offering friendly Claude training for small business owners and busy moms, plus guided custom Claude agent builds. The audience includes people who want practical help with AI and do not have a technical background.

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
| `owner-photo.png` | Gina's founder photo, displayed on the About view |
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

## Page Views

The single HTML file uses hash routes, so each view has a direct URL fragment and its own document title and description:

1. **Home** (`#home`) — headline, offer links, three-step process, placeholder testimonials, booking CTA
2. **Services** (`#services`) — free fit call, Starter Session, 3-Pack, and Agent Build Consultation
3. **Courses** (`#courses`) — Claude for Small Business and Claude for Moms, plus a name/email waitlist form
4. **About** (`#about`) — Gina's photo and 20+ years of business growth, sales leadership, retail, small-business, and team-development experience
5. **FAQ** (`#faq`) — six questions about Claude, privacy, plans, sessions, and service differences
6. **Book** (`#book`) — free call details, intake questions, and booking CTA

`PAGE_META` in `index.html` holds route titles and descriptions. `SITE_CONFIG` holds the booking and waitlist URLs and all displayed prices.

## SEO (added April 2026)

- **Title:** "Claude Training for Small Business Chicago | Innovative Projects Hub"
- **Meta description:** Friendly Claude training and AI help for small business owners in Chicago.
- **Open Graph tags:** og:title, og:description, og:image (owner-photo.png), og:url
- **Twitter Card tags:** summary_large_image
- **Canonical URL:** set to GitHub Pages URL
- **Favicon:** inline SVG (no file needed)
- **H1:** "Get hours back every week with Claude"

## Integrations

### Booking and Waitlist
- `SITE_CONFIG.BOOKING_URL` currently uses the Google Calendar appointment link from the previous IPH site; confirm the appointment schedule and availability before publishing.
- The Courses view embeds the Google Form configured by `SITE_CONFIG.WAITLIST_FORM_URL`; responses are collected in Google Forms.
- Update the `SITE_CONFIG.PRICES` values in one place when prices change.

## Interactions

- Hash navigation switches between six page views and updates the document title and description.
- The mobile hamburger button opens and closes the responsive navigation.

## Responsive Breakpoints

- **1024px:** content grids reduce to two columns
- **768px:** navigation switches to the mobile menu and content grids become single-column
- **480px:** buttons expand to the available width

## Content Notes

- IPH teaches people to use Claude and helps business owners build Claude agents; it does not offer web design or digital marketing services.
- Do not add past-client names or unsupported testimonials/results.
- Keep copy friendly and clear for non-technical readers.

## Placeholders / TODOs

- Confirm the Google Calendar appointment schedule and availability.
- Confirm the embedded Google Form accepts responses and records them as expected.
- Sessions are available online or in person.
- Replace testimonial placeholders when real testimonials are available.

## Deployment

To preview locally, open `index.html` in a browser or run `python3 -m http.server 8000` from the repository folder and visit `http://localhost:8000`.

To publish, merge the update branch into `main` and push it; GitHub Pages serves the root `index.html` from `main`.

## Copy Conventions

- **Honest positioning:** Do not imply past clients, testimonials, or outcomes that are not established.
- **Non-technical audience:** Plain, friendly language. Explain unfamiliar terms.
- **No em dashes** — use commas, periods, or ellipses

## Code Conventions

- All CSS in a single `<style>` tag in `<head>`
- All JS in a single `<script>` tag before `</body>`
- Sections use semantic HTML (`<section>`, `<nav>`, `<footer>`)
- Icons are inline SVGs (no icon library)
- CSS uses custom properties extensively for theming
- Mobile menu uses `.open` class toggle
- External links should open safely in a new tab when appropriate.
