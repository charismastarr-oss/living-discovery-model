# The Living Discovery Model

A reference framework for eDiscovery inside an AI-native corporation, by Charisma Starr.

## What's here

- `index.html` — Home
- `model.html` — The Model (full five-stage breakdown)
- `vs-edrm.html` — Comparison against EDRM / EDRM 2.0
- `about.html` — About
- `assets/css/style.css` — Shared stylesheet (brand tokens, stage colors, responsive layout)
- `assets/img/` — Diagram and flowchart images

Fonts (Cormorant Garamond, Jost) load from Google Fonts via CSS `@import`, no build step, no dependencies.

## Deploying to GitHub Pages

1. Create a new repository (e.g. `living-discovery-model`), or use an existing one.
2. Copy everything in this folder into the repo root (keep the `assets/` folder structure intact).
3. Commit and push to the `main` branch.
4. In the repo, go to **Settings → Pages**.
5. Under **Build and deployment**, set **Source** to "Deploy from a branch," branch `main`, folder `/ (root)`.
6. Save. GitHub will publish at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Using a custom domain

Once you've confirmed a domain:

1. Add a file named `CNAME` (no extension) to the repo root containing just your domain, e.g.:
   ```
   livingdiscoverymodel.com
   ```
2. In **Settings → Pages → Custom domain**, enter the same domain and save. GitHub will auto-create the `CNAME` file if you do it this way instead.
3. At your domain registrar, point DNS at GitHub Pages:
   - For an apex domain (`livingdiscoverymodel.com`): add A records to GitHub's IPs (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153).
   - For a `www` subdomain: add a CNAME record pointing to `<your-username>.github.io`.
4. Check "Enforce HTTPS" once the certificate provisions (can take a few hours).

## Editing content

Everything is plain HTML, no templating. To update stage copy, edit the relevant `<div class="stage-body">` or card block directly. Colors and type live entirely in `assets/css/style.css` under `:root`, change a value there and it updates across every page.
