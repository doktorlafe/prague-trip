# Prague, Beyond the Postcard

Prague travel guide published at **https://prg.thugsclub.eu**.

The site is a single self-contained `index.html`: no build step, no external requests, no tracking. It also works offline if you open it straight from disk.

## Contents

- [`index.html`](index.html): the full guide (sights with prices and hours, transport, history, timed itineraries, Prague 7 deep dive, food, day trips, scams, phrasebook)
- [`itinerary.md`](itinerary.md): day-by-day planning notes
- [`prague-7-guide.md`](prague-7-guide.md): Holešovice / Letná notes
- [`budget.md`](budget.md): cost planning
- [`packing-checklist.md`](packing-checklist.md): what to bring

## Deployment (GitHub Pages)

`CNAME` sets the custom domain and `.nojekyll` makes Pages serve the files as-is.

1. **DNS** at the `thugsclub.eu` DNS provider: add a `CNAME` record `prg` → `doktorlafe.github.io.`
2. **Pages**: repo **Settings → Pages → Build and deployment → Deploy from a branch**. Pick the branch that holds `index.html` and the folder `/ (root)`.
3. **Custom domain**: confirm it reads `prg.thugsclub.eu`, wait for the DNS check, then tick **Enforce HTTPS** once the certificate is issued.
4. **Recommended**: verify `thugsclub.eu` under GitHub **Settings → Pages → Verified domains** (account level), to prevent subdomain takeover.

Check it with `dig +short prg.thugsclub.eu CNAME`, which should return `doktorlafe.github.io.`
