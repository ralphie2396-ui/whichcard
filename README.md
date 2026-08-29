# Which Card

Ranks your Amex cards for any purchase. Runs entirely in the browser, stores everything on the device.

## Put it on your iPhone home screen

You need it on a URL — iOS can't add a downloaded file to the home screen.

**GitHub Pages (free, ~5 minutes)**
1. Create a new public repo at github.com/new
2. Upload all six files to the root of the repo
3. Settings → Pages → Source: `Deploy from a branch` → Branch: `main`, folder `/ (root)` → Save
4. Wait a minute, then open `https://<your-username>.github.io/<repo-name>/`
5. In Safari, tap Share → Add to Home Screen

Netlify Drop (netlify.com/drop) works too — drag the folder in, no account needed for a temporary URL.

## Files
- `index.html` — the whole app
- `manifest.json` — makes it installable
- `sw.js` — caches it for offline use
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`

## First run
1. **Wallet** — tick the cards you carry. Nothing is ranked until you do.
2. **Values** — adjust cents-per-point if you disagree with the defaults. This changes the answers a lot.
3. **Offers** — add Amex Offers by hand, or paste an API key in Values to import them from screenshots.

## Offline
After the first load, the service worker caches everything. The merchant list, ranking and offers all work with no signal. Only the two optional Claude features need a connection.

## Updating rates
Card earn rates are in the `CARDS` array near the top of the `<script>` block in `index.html`. Rates were checked August 2026.
