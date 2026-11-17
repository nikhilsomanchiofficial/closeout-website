# closeout-website

Static one-page site for Leede (closeout audits for California subcontractors). Two files, no build step, no JavaScript.

- `index.html` — the page
- `styles.css` — styles (light and dark, responsive)

## Before you publish

Search `index.html` for these four placeholders and replace them:

| Placeholder | Where | Replace with |
|---|---|---|
| `[CALENDAR_LINK]` | nav button, hero, bottom CTA | your booking link (Cal.com, Calendly, etc.) |
| `[email]` | bottom CTA mailto, footer | the address you want replies at |
| `[Name]` | footer | your name |
| `[phone]` | footer | your phone |

The "See a sample report" button links to the published sample report. Swap it for a hosted PDF when you have one.

## Deploy

Any static host works. Fastest options:

- **GitHub Pages:** repo Settings → Pages → Deploy from branch → `main` / root. Add a `CNAME` file containing your domain, then point the domain's DNS at GitHub Pages (A records `185.199.108–111.153`, or a CNAME to `<user>.github.io`).
- **Netlify / Vercel / Cloudflare Pages:** connect the repo, no build command, output directory `/`.

Host it on `getleede.com` (replace the old page). A sending domain with a real site behind it helps deliverability, and the brand now matches the sender.

## Editing

Numbers in the sample ledger come from `closeout-cash/04_mock_report/job_ledger_apex.csv`. If the mock report changes, update the table by hand; it's five rows.

No prices on the page (removed Nov 16). The fee section says only: flat fee set by revenue, quoted on the first call, 10× refund, optional monthly tracking. The price list lives in the project context doc, not here.
