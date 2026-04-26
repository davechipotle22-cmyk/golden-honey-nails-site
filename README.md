# Golden Honey Nails — proposed website

A clean, fast, mobile-first website built as a direct upgrade to the current Wix site at `goldenhoneynails.wixsite.com/goldenhoneynails`.

## What's in this folder

| File | Page |
| --- | --- |
| `index.html` | Home — hero, value props, featured services, hours/location, CTA |
| `services.html` | Full services & pricing menu |
| `about.html` | Story, standards, "visit us" |
| `gallery.html` | Masonry gallery with click-to-zoom lightbox |
| `contact.html` | Phone, address, full hours, socials, contact form, map |

No build step. No package install. Just open `index.html`.

## How to view it

**Locally:** double-click `index.html` — it opens in your browser. Nav links jump between pages.

**Online (free) — Netlify drop:**
1. Go to <https://app.netlify.com/drop>
2. Drag this whole `golden-honey-nails` folder into the page
3. You get a live URL in ~10 seconds. Share it, or point your custom domain at it.

**Online (free) — GitHub Pages:** push the folder to a repo, enable Pages on the `main` branch, root.

## Why this beats the current Wix site

1. **Speed** — static HTML, no Wix runtime. Loads in under a second; the current site takes several seconds to boot the Wix viewer.
2. **Mobile experience** — real mobile nav, tap-to-call phone, tap-to-map address, sticky "Book" button on the pricing page.
3. **Information design** — pricing is now a scannable two-column menu instead of one long bulleted list. Hours and address appear in the footer of every page.
4. **Local SEO** — every page emits a clean `<title>`, `<meta description>`, Open Graph tags, and (on home) a full `schema.org/NailSalon` JSON-LD block (name, address, phone, hours, geo, social profiles). This is what tells Google to show your salon in the local "map pack" results — it isn't on the current site.
5. **Branding** — custom honey-gold palette, Playfair Display + Inter typography, hand-tuned spacing. Looks like a salon that cares about the details, not a generic Wix template.
6. **Ownership & cost** — these are plain HTML files. You own them. Free to host on Netlify or GitHub Pages. No monthly Wix subscription required (current Wix plans for a custom domain run $17–$36/month).
7. **Booking preserved** — every "Book Now" button still points to your existing Fresha link (`app.shedul.com/online_bookings/21769/link`). Zero migration friction.

## Things to swap before launch

- **Photos.** Hero images and the gallery use stock photos from Unsplash so the demo renders without shipping image files. Replace the `<img src=...>` URLs with photos of your actual salon and your work. Square or 4:5 aspect works best for the "Featured services" cards.
- **Email.** The contact form uses a `mailto:` to a placeholder address (`hello@goldenhoneynails.com`). Either:
  - Set up that email on your domain, or
  - Swap the form `action` attribute to a free Formspree endpoint (`https://formspree.io/f/YOURID`) — that delivers submissions to whatever inbox you want, no server required.
- **Domain (optional).** A `goldenhoneynails.com` registration is ~$12/year. Pointing it at Netlify or GitHub Pages takes about 5 minutes.

## What you can change yourself

Each page is a single self-contained `.html` file. To edit pricing, open `services.html` in any text editor and change the numbers — nothing else to rebuild. To change hours, the same hours block lives in the footer of every page (search for "10:00 AM – 7:00 PM").

## Tech notes (for whoever maintains it)

- Tailwind CSS via CDN (no compile step).
- Google Fonts: Playfair Display + Inter.
- Vanilla JS only — no jQuery, no framework. Total custom JS is ~30 lines per page (sticky-header tweak, mobile nav, fade-on-scroll, lightbox).
- All pages pass HTML5 validation and target Lighthouse Performance / Accessibility / SEO ≥ 95.
- `schema.org/NailSalon` JSON-LD on `index.html` for local search.
- `<link rel="icon">` is an inline SVG data URL — no favicon file to ship.
