# Innovative Projects Hub — Website

Single-page marketing website for a social media management agency targeting small businesses.

## Tech Stack

- **Single file:** `index.html` (all HTML, CSS, and JS embedded)
- **No build tools, frameworks, or dependencies**
- **Fonts:** Google Fonts — Playfair Display (serif headings) + Inter (sans-serif body)

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

## Page Sections (in order)

1. **Navigation** — fixed top, glassmorphism backdrop blur, logo + links (Services, Packages, Process, About, Results) + CTA, mobile hamburger menu
2. **Hero** — full viewport, headline + subtitle + 2 CTAs ("Book a Free Consultation" + "Meet Gina, Your Growth Partner"), floating stat cards (engagement +147%, followers +2.4K, response rate 3x)
3. **Marquee Ticker** — infinite scrolling service keywords
4. **What We Do** (#services) — 4 service cards (Content Planning, Content Creation, Scheduling, Growth Strategy) with numbered icons
5. **Meet Your Strategist** (#about) — two-column grid: left has "Founder & Business Growth Strategist" gradient badge + owner photo (`owner-photo.png`), right has bio + 4 strength cards (20+ Years of Business Growth, More Than Just Social Media, Built for New and Growing Businesses, A Real Partner Not Just a Service) + CTA button
6. **Who This Is For** (#who) — checklist layout (New and Existing Business Owners, Side Hustlers Going Full-Time, Busy Entrepreneurs, Overwhelmed by Social Media) + SVG hub-and-spoke illustration
7. **Pricing** (#pricing) — 3-tier cards (Foundation $497-697, Growth $997-1497 featured, Visibility+Growth $1997-2997)
8. **How It Works** (#how-it-works) — 4 numbered steps with arrow connectors (Consultation, Strategy, Content Creation, Scheduling + Growth)
9. **Why Choose Us** (#why) — 4 value props with icons (Done-for-You, Strategy + Execution, Built for Small Businesses, Focused on Real Growth)
10. **Results** (#results) — 4 outcome cards (Stronger Online Presence, More Engagement, Consistent Branding, More Customer Inquiries)
11. **Final CTA** (#book) — centered call-to-action with booking button
12. **Footer** — logo, nav links, copyright 2026

## Animations & Interactions

- **Scroll animations:** `.fade-up`, `.slide-left`, `.slide-right` — triggered via IntersectionObserver at 8% threshold
- **Stagger effect:** children inside `.stagger` containers get sequential 0.12s delays
- **Parallax blobs:** 3 gradient blobs in hero move on scroll (desktop only)
- **Navbar:** adds `.scrolled` class with box-shadow after 20px scroll
- **Buttons:** translateY(-3px) on hover with shadow transitions
- **Marquee:** CSS `@keyframes marquee-scroll` infinite loop

## Responsive Breakpoints

- **768px:** single-column layouts, hero visual reorders above text, mobile menu activates, floating cards hidden
- **480px:** full-width buttons, stacked CTA buttons

## Removed Sections

- **Stats Bar** — was between What We Do and Who This Is For (150+ Posts Published, 95% Client Retention, 3x Engagement Lift, 24/7 Content Support). Removed as placeholder data.

## Placeholders / TODOs

- No favicon or Open Graph meta tags
- No analytics or tracking scripts
- `office-photo.jpg` exists but is not currently used (replaced by SVG illustration)

## Conventions

- All CSS is in a single `<style>` tag in `<head>`
- All JS is in a single `<script>` tag before `</body>`
- Sections use semantic HTML (`<section>`, `<nav>`, `<footer>`)
- Icons are inline SVGs (no icon library)
- CSS uses custom properties extensively for theming
- Animations use CSS transitions + JS IntersectionObserver (no animation library)
- Mobile menu uses `.open` class toggle
