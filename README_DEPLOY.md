# DKEDU — Programs Updated (Deploy Guide)

This ZIP includes:
- `index.html` — program catalog updated to your CRM list (6 main programs + add‑ons/discounts).
- `products.json` — the same data in JSON so you (or devs) can automate future updates.

## Deploy (Vercel quickest)
1) Go to vercel.com → **+ Deploy → Deploy Project → Import → Drop**
2) Drag‑drop the *unzipped* folder with `index.html`
3) You’ll get a live `*.vercel.app` URL.

## Custom domain (optional)
- In Vercel → **Project → Settings → Domains → Add** your domain.
- DNS at provider: **A (root)** → `76.76.21.21`, **CNAME (www)** → `cname.vercel-dns.com`.

## Editing products later
- Open `products.json` and `index.html`:
  - Update prices or names in `products.json`.
  - Update the HTML cards if you need copy tweaks.
- Re‑deploy via Vercel drag‑drop.

## Notes
- Discounts are shown as negative values and explained in the “How discounts work” card.
- If you want a calculator that updates totals as users toggle add‑ons, tell me and I’ll add it.
