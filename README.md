# Occupied. — Website

Mobile-first marketing site for Occupied., a dynamic pricing and listing optimisation service for STR owners.

## File structure

```
occupied-site/
├── index.html       # Homepage
├── privacy.html     # POPIA privacy policy
├── thanks.html      # Post-form-submit page (ready for when you add a form)
├── robots.txt       # SEO crawler instructions
├── sitemap.xml      # SEO sitemap
├── vercel.json      # Vercel deploy config with security headers
└── README.md        # This file
```

## ⚠️ Before going live — REQUIRED placeholder replacements

Search and replace these in the codebase. They are intentionally fake until you fill them in:

| Placeholder | Where | Replace with |
|---|---|---|
| `[REPLACE WITH REGISTERED COMPANY NAME]` | `privacy.html` | Your CIPC-registered company name |
| `[REPLACE WITH REG NUMBER]` | `privacy.html` and `index.html` footer | Company reg number, e.g. `2024/123456/07` |
| `[REPLACE WITH ADDRESS]` | `privacy.html` | Registered company address |

WhatsApp number is set to `+44 7446 711319` (UK number, formatted as `447446711319` in the `wa.me/` URLs). Update via find-and-replace if it changes.

The pre-filled WhatsApp message is: *"Hi, I'm interested in Occupied. — can we chat?"* — change it in `index.html` by searching for `Hi%2C%20I%27m%20interested%20in%20Occupied`.

## Pre-launch checklist

### Must-fix before launch
- [ ] Fill in company name, reg number, and address in `privacy.html`
- [ ] Update the footer reg number in `index.html`
- [ ] Replace the projected chart data with a real anonymised client case (or leave as projected with clear disclaimer)
- [ ] Get permission from Nadia M., James R., and Thandiwe K. to use their names/quotes (or replace with anonymised initials)

### Strongly recommended
- [ ] Buy `occupied.co.za` domain (~R100/year at domains.co.za or Hetzner)
- [ ] Add an Open Graph image at `/og-image.png` (1200×630px) — currently only text-based previews
- [ ] Test the OG preview at [opengraph.xyz](https://www.opengraph.xyz) after deploy
- [ ] Add analytics — Plausible ($9/mo, POPIA-friendly) is preferred over GA4
- [ ] Set up Google Search Console + submit sitemap.xml
- [ ] Run [PageSpeed Insights](https://pagespeed.web.dev) after deploy

### Nice-to-have for v2
- [ ] Real photography (one Cape Town STR interior shot for the hero)
- [ ] Founder bio / "Meet Rob" mini-section
- [ ] Replace `mailto:` form with Supabase-backed contact form → Pipedrive via Zapier
- [ ] Add 2-3 real client logos in a small "trusted by" strip
- [ ] FAQ accordion (cancellation, contract length, what if results don't hit)

## Deploy to Vercel

### 1. Push to GitHub

```bash
cd occupied-site/
git init
git add .
git commit -m "Initial site"
git branch -M main

# After creating an empty private repo on github.com called "occupied-site":
git remote add origin https://github.com/YOUR-USERNAME/occupied-site.git
git push -u origin main
```

Or drag-and-drop the files into a new repo via GitHub's web UI.

### 2. Connect Vercel

1. Sign up at [vercel.com](https://vercel.com) using your GitHub account
2. Click **Add New… → Project**
3. Import `occupied-site` from GitHub
4. **Framework Preset:** Other
5. Click **Deploy**

Live URL in ~30 seconds: `occupied-site-xyz.vercel.app`

### 3. Add your custom domain

1. Buy `occupied.co.za` from a SA registrar
2. In Vercel: **Project → Settings → Domains → Add `occupied.co.za`**
3. Add the DNS records Vercel shows you to your registrar's DNS panel
4. Wait 5–30 min for propagation. HTTPS is automatic.

## Updating the site

Edit any file in GitHub (pencil icon works fine) and commit. Vercel auto-deploys within ~30 seconds.

## When you're ready for Supabase

Replace the WhatsApp button with a real form that posts to Supabase. The `thanks.html` page is already styled and waiting. Ping Claude when ready and the setup takes about 30 minutes end-to-end.
