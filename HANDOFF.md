# IPH Website Handoff

Last updated: 2026-11-18

## Current Status

- The updated site is live at https://iphgrowthofficer-star.github.io/innovative-projects-hub/.
- GitHub Pages deploys the root `index.html` from the `main` branch.
- Published commit: `640d917` (`Update IPH site for Claude coaching`).
- The repository was clean on `main` after publishing. The `claude-coaching-update` branch points to the same published commit.
- No build tools or framework are used. The whole website is a static HTML file with embedded CSS and JavaScript.

## Website Files

- `index.html`: all site content, styling, route metadata, price/link configuration, and scripts.
- `owner-photo.png`: Gina's portrait used on the About page.
- `office-photo.jpg`: available image, not currently used.
- `IPH Website/CLAUDE.md`: project/design documentation and content conventions.
- `HANDOFF.md`: this resume note.

## Pages

The site uses hash routes within `index.html`, not separate HTML pages:

- Home: `#home`
- Services: `#services`
- Courses: `#courses`
- About: `#about`
- FAQ: `#faq`
- Book: `#book`
- Waitlist anchor on Courses: `#waitlist`

Navigation switches the visible view and updates the document title and description. The navigation and pages include booking CTAs.

## Business Content

- IPH now teaches small business owners and busy moms to use Claude in everyday work and life, and helps business owners build custom Claude agents.
- The Home page uses the headline “Get hours back every week with Claude,” includes the offers, three steps, and three testimonial placeholders.
- Services list the Free Claude Fit Call, Claude Starter Session ($150), Starter Session 3-Pack ($399), and Agent Build Consultation ($200/hour, two-hour minimum).
- Courses cover Claude for Small Business and Claude for Moms. Course pricing is shown as “$47 to $97, launching soon.”
- The About page includes Gina's photo and the bio about nearly 20 years in sales leadership, coaching and developing teams, retail and small-business experience, being a mom, and using Claude in daily life.
- FAQ says sessions are available online or in person.
- Do not add past-client names or imply unsupported testimonials or results. Keep copy friendly and non-technical.

## Integrations

Both URLs are in the `SITE_CONFIG` object in `index.html`:

- `BOOKING_URL`: `https://calendar.app.google/ptUn1uAM312FhpsL9`. Booking buttons open this Google Calendar appointment page. Confirm that the appointment type and availability are still correct.
- `WAITLIST_FORM_URL`: `https://docs.google.com/forms/d/e/1FAIpQLSdr2mfkw3ZXfODeOGBS8DubnXnxNd7j9Jei8WbFBDp-SIFO8A/viewform?embedded=true`. The Courses page embeds this live Google Form. It asks which course interests the visitor, name, and email. The short link provided was `https://forms.gle/FWXBfhTTXi2qDUtn6`.
- Prices are centralized in `SITE_CONFIG.PRICES` in the same file.

The form was opened and its fields were verified in the browser. Confirm that it is still accepting responses and that submissions are recorded as expected.

## Remaining Follow-Ups

- Confirm the Google Calendar appointment schedule and availability.
- Confirm the Google Form accepts responses and records them as expected.
- Replace the three “Testimonial coming soon” cards when real testimonials are available.
- Course prices are intentionally labeled as launching soon and may need updating before launch.

## Local Preview

Open `index.html` directly in a browser, or from the repository folder run:

```sh
python3 -m http.server 8000
```

Then visit http://localhost:8000. There are no package installs or build steps.

## Resume / Publish Workflow

```sh
cd "/Users/growthofficer/Learning/IPH Start up/innovative-projects-hub"
git status --short --branch
```

Edit `index.html` for website changes and `IPH Website/CLAUDE.md` for project documentation. After validating locally:

```sh
git diff --check
git add index.html "IPH Website/CLAUDE.md" HANDOFF.md
git commit -m "Describe the site update"
git push origin main
```

GitHub Pages deploys automatically from `main`. Check the repository's Actions page if the public site does not update shortly after the push.