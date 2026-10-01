# Altware Development — static site

Rewrite of www.altwaredevelopment.com for GitHub + Cloudflare Pages.
No build step. Cloudflare serves this folder as-is.

Sales stay on chatters.io. Firmware stays on offgridcomms.club.
Contact is the existing LinkedIn profile. No email was published on the old site.

## Publish

1. Create a new GitHub repository. Public or private both work with Cloudflare Pages.
2. Push this folder as the repository root, not inside another folder.
3. In Cloudflare: Workers & Pages → Create → Pages → Connect to Git.
4. Framework preset: None. Build command: empty. Output directory: `/`
5. Deploy. You get a `*.pages.dev` URL first.
6. Custom domains → add `altwaredevelopment.com` and `www.altwaredevelopment.com`.
7. At the registrar, either move DNS to Cloudflare or add the CNAME / A records Cloudflare shows you.
8. After the new site is live, cancel Squarespace. Do that last, so the old host keeps answering until DNS moves.

`_redirects` maps the old Squarespace paths onto the new ones.

## Edit

- Copy lives in the HTML files.
- Shared styles: `css/site.css`
- Menu: `js/site.js`
- Images: `assets/`
- LVPS documents copied off Squarespace: `docs/`

## Old URLs

| Squarespace | New |
| --- | --- |
| `/what-is-blackout-comms` | `/blackout/` |
| `/blackout-comms-lora` | `/blackout/lora.html` |
| `/mesh-communication` | `/blackout/mesh.html` |
| `/security` and encryption | `/blackout/security.html` |
| `/digital-signatures` | `/blackout/signatures.html` |
| `/blackout-comms-mesh-cluster-onboarding` | `/blackout/onboarding.html` |
| `/blackout-comms-mesh-range` | `/blackout/range.html` |
| `/blackout-comms-vs-meshtastic-compare` | `/blackout/compare.html` |
| `/mesh-product-reviews` | `/reviews/` |
| `/lightweight-visual-positioning-system` | `/lvps/` |
| `/who-is-altware` | `/about/` |
| `/off-grid-communication` | `/guides/` |
