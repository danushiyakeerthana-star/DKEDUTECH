# DKEDU — Rich Sales Website (Deploy Guide)

This ZIP contains:
- `index.html` — single-file site with live IST clock, countdown, pricing toggle, testimonials, sticky CTAs, and a lead-capture modal.
- `README_DEPLOY.md` — these steps.

## 1) Fastest deploy (Vercel)
1. Go to **vercel.com → + Deploy → Deploy Project → Import → Drop**.
2. Drag-drop the *unzipped* folder that contains `index.html`.
3. You’ll get a live URL like `https://dkedu.vercel.app`.

**Attach a custom domain (optional):**
- Add domain in Vercel → **Project → Settings → Domains → Add** `yourdomain.tld`.
- At your domain provider, set:
  - **A** (apex/root) → `76.76.21.21`
  - **CNAME** for `www` → `cname.vercel-dns.com`
- Back in Vercel, click **Verify** → SSL auto-enables.

## 2) GitHub Pages (free URL)
1. Create a repo, e.g. `dkedu-site` → upload `index.html`.
2. Repo **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main` → Folder: `/ (root)`.
3. Live at `https://<your-username>.github.io/dkedu-site/`.

## 3) Netlify (free URL)
1. app.netlify.com → **Add new site → Deploy manually**.
2. Drag-drop the folder with `index.html`.
3. You’ll get `https://dkedu.netlify.app`.

## 4) Configure the “Realtime” bits
Open `index.html`, near the end you’ll see:
// Config (edit these)
```js
const COHORT_START = new Date("2025-09-15T09:00:00+05:30"); // change date/time
const BUSINESS_HOURS = { days:[1,2,3,4,5,6], start:9, end:18 }; // Mon–Sat 9–18 IST
```
- Change `COHORT_START` to your next batch date.
- Adjust `BUSINESS_HOURS` to your schedule.

## 5) Replace the lead modal with Zoho (optional)
- In Zoho Desk (or Zoho Forms), create a webform.
- Copy the **embed snippet** and paste it in place of the lead form (search for `<!-- Lead modal (Zoho integration ready) -->` in `index.html`).

## 6) WhatsApp & Email
- Replace the placeholder WhatsApp link `https://wa.me/919876543210`.
- Replace `admissions@dkedu.com` with your real address.

## 7) Quick tweaks
- Edit hero copy, course names, and pricing text inside `index.html`.
- Swap the simple logo block with your SVG/PNG if you have one.

That’s it — publish and share your link! 🎉
