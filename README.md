# Mamba Tech Solutions — Home Services & Trades Edition (Mock Marketing Site)

A 4-page static mock site for Mamba Tech Solutions, adapted for the home services and field trades
market (HVAC, plumbing, electrical, and similar multi-crew businesses) — the same Microsoft
Teams calling, presence-based dispatch routing, and managed-permissions service originally
built for the medical office market, retargeted with new copy and a confident, modern theme.

## Structure

```
index.html          Home
services.html        Services
how-it-works.html    How It Works
contact.html         Contact (mock form — no backend wired up)
css/styles.css       Shared stylesheet
js/script.js         Mobile nav, scroll reveal, mock form handler
```

No build step — plain HTML/CSS/JS. Open `index.html` directly in a browser to preview locally.

## Deploying to GitHub Pages and pointing a custom domain

**1. Push these files to a GitHub repo**, at the root (or a `docs/` folder — just match the setting in step 2).

**2. Turn on GitHub Pages**
Repo → Settings → Pages → set "Source" to your branch (and `/root` or `/docs`, matching where the files live). This gives a URL like `https://yourusername.github.io/your-repo`.

**3. (Optional) Add a custom domain**
Still in Settings → Pages, enter the domain in the "Custom domain" field — this auto-creates a `CNAME` file in the repo. Without this step, a custom domain pointed at GitHub's IPs will resolve to a generic "no Pages site here" 404.

**4. Point the registrar's DNS at GitHub Pages**
Add four `A` records for the apex domain (`@`) pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, and a `CNAME` record for `www` pointing to `yourusername.github.io`.

**5. Verify the domain at the GitHub account level (recommended)**
GitHub account Settings → Pages → add and verify the domain via a TXT record, to prevent a domain takeover if the DNS record is ever left pointing at GitHub after the site comes down.

## Notes

- This started as a retarget of the FixedIT Tech (medical-office) site, but now runs under its own brand, Mamba Tech Solutions, distinct from FixedIT Tech. Keep this in its own repo, separate from any FixedIT Tech codebase, since they're no longer the same company.
- Contact form is non-functional by design (mock site). To make it live, wire it to a form service (e.g. Formspree, Netlify Forms) or a real backend.
- Email/phone on the Contact page are placeholders — replace with real details before launch.
- Theme: charcoal + amber, Space Grotesk / Inter / JetBrains Mono — distinct from the medical site's navy/blue, Newsreader-based theme on purpose.
