# Digiability — Coming Soon Landing Page

A single-page Bootstrap 5 landing page for **digiability.in** while the
full portal is being built.

## Files

```
digiability-landing/
├── index.html      ← main page
├── styles.css      ← Digiability theme (navy + gold + purple)
└── README.md       ← this file
```

## Tech

- HTML5
- CSS3 (custom, layered on Bootstrap)
- Bootstrap 5.3.3 (loaded from CDN)
- Bootstrap Icons 1.11 (loaded from CDN)
- Google Fonts — Plus Jakarta Sans + Inter

No build step. No backend. Open `index.html` in any browser.

## Theme

- Navy `#0B0B2E` (background)
- Gold `#F5B82E` (primary accent)
- Purple `#9B4DFF` / `#551A8B` (secondary accent)
- Cream `#FFF8EC` (text)
- Lavender `#C9C2E8` (muted text)

## Sections on the page

1. **Top nav** — logo placeholder + "Launching soon" pulse dot
2. **Hero** — "Coming Soon" eyebrow + large headline + tagline + email signup
3. **Services** — 6 service cards:
   - Welfare Schemes
   - Document Support
   - Health Camps
   - Insurance Schemes
   - Information Center
   - One Connected Ecosystem (NGO/SP/Field/BEN)
4. **Partners strip** — "Navasaptarishi · Built by Techonsy"
5. **Footer** — copyright + contact email

## To-do before going live

- [ ] **Replace the logo placeholder.** Currently a gold square with "D"
      inside. Swap the `.brand-logo` div in `index.html` for an `<img>`
      pointing to the real logo file. Also update the `<link rel="icon">`
      data-URI in the `<head>` with the real favicon.
- [ ] **Wire the notify form** to a real backend (MSG91, Mailchimp, or a
      tiny endpoint that writes to a DB / Google Sheet). Search for the
      `TODO` comment in `index.html`.
- [ ] **Update the contact email** if `hello@digiability.in` is not the
      preferred address.
- [ ] **Add Google Analytics / Plausible / Umami snippet** if you want
      to track visits.
- [ ] **OG image** — generate a `/og-image.png` (1200×630) for the social
      preview, then add `<meta property="og:image" content="...">`.

## Deploy

Any static host will work — Vercel, Netlify, Cloudflare Pages, GitHub
Pages, S3+CloudFront, or just `nginx` on your own VPS.

### Quick deploy options

**Cloudflare Pages**
```
1. Create a Git repo with these files at the root.
2. Cloudflare Pages → Create project → connect repo.
3. Build command: (leave empty)
4. Build output: /
```

**Netlify drop**
```
Drag this folder onto https://app.netlify.com/drop
```

**nginx on a VPS**
```nginx
server {
  listen 80;
  server_name digiability.in www.digiability.in;
  root /var/www/digiability-landing;
  index index.html;
}
```

Point the `digiability.in` A/AAAA records at the host once it's live.
