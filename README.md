# BreakThru landing site

Static marketing site for BreakThru, served at **https://breakthruadhd.com** via GitHub Pages.

## Structure
- `index.html` — the landing page. Fully self-contained: fonts (DM Sans, Fraunces) and the
  App Store icon are inlined as base64, so the page loads in a single request with no external calls.
- `privacy/`, `terms/`, `support/` — legal pages as folders so the clean URLs
  (`/privacy`, `/terms`, `/support`) resolve on GitHub Pages (which has no `cleanUrls` rewrite).
- `CNAME` — binds the custom domain `breakthruadhd.com`.
- `.nojekyll` — serves files as-is, skips Jekyll processing.
- `404.html` — on-brand not-found page.

## Deploy
GitHub Pages builds automatically on every push to `main` (Settings → Pages → Source: `main` / root).
Just edit and push; the live site updates in a minute or two.

## DNS
Apex `breakthruadhd.com` points at GitHub Pages IPs; `www` is a CNAME to `atherbilal.github.io`.
Managed at the domain registrar (Name.com).
