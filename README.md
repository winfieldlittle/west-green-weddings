# The Gardens at West Green — Website

Static website for **The Gardens at West Green**, a wedding venue in San Antonio, TX. This project migrates an existing WordPress site to a pure HTML/CSS/JavaScript static site hosted on Netlify.

---

## Venue Info

| | |
|---|---|
| **Address** | 21650 Milsa Dr, San Antonio, TX 78256 |
| **Phone** | 210-698-9191 |
| **Email** | weddings@thegardensatwestgreen.com |

---

## Tech Stack

- **HTML5 / CSS3 / Vanilla JavaScript** — no frameworks, no jQuery, no Bootstrap
- **Netlify** — hosting and form handling
- **Netlify Forms** — all forms use `data-netlify="true"`
- **Flatpickr** (via jsDelivr CDN) — date pickers
- **External CDNs** — jsDelivr or cdnjs only

---

## Brand & Design

| Token | Value |
|---|---|
| **Primary font** | Georgia (serif) |
| **Accent color** | `#b08d75` (warm rose-gold tan) |
| **Palette** | Off-whites, warm grays |
| **Style** | Warm, elegant, minimal — no gradients, no heavy shadows |

---

## Pages

| Page | File | Status |
|---|---|---|
| Home | `index.html` | — |
| About / Our Story | `about.html` | — |
| Gallery | `gallery.html` | — |
| Venues / Spaces | `venues.html` | — |
| Pricing / Packages | `pricing.html` | — |
| FAQ | `faq.html` | — |
| Contact | `contact.html` | ✅ Complete |

> **Note:** Confirm the final page list with Karen before building remaining pages.

---

## Contact Page

The contact form (`contact.html`) is fully built and includes:

- **Fields:** Full Name, Email, Phone, Wedding Date (Flatpickr), Guest Count, Info Request, Referral Source
- **Guest Count options:** Under 40 / 40–60 / 60–80
- **Referral options:** Wedding Wire / The Knot App / Google Search / Online Wedding Directory / Friend / Wedding Coordinator / Other (with text field)
- Inline validation on all required fields
- Sidebar with contact info and social links
- Netlify Forms integration

---

## Conventions

- All pages share a consistent `<nav>` and `<footer>`
- Mobile responsive — single column on small screens
- All external resources load from **jsDelivr** or **cdnjs** only
- Netlify Forms (`data-netlify="true"`) on any page with a form
- No jQuery, no Bootstrap, no CSS frameworks

---

## Local Development

No build step required. Open any `.html` file directly in a browser, or use a simple local server:

```bash
npx serve .
# or
python3 -m http.server
```

> **Netlify Forms** require deployment to Netlify to function — they will not process submissions in local development.

---

## Deployment

The site is hosted on **Netlify** with automatic deploys from the connected Git repository. Push to `main` to deploy.

For Netlify Forms to work, each form must include:
```html
<form name="your-form-name" method="POST" data-netlify="true">
  <input type="hidden" name="form-name" value="your-form-name" />
  ...
</form>
```

---

## Project Contact

For questions about this project, reach out to **Karen** at the venue.
