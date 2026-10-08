# hufnor-site

Source of truth for **https://blackridge-design.com** (Hufnor Design).

| File | What it is |
|---|---|
| `index.html` | The whole website (single file). **This is the master copy.** |
| `ghl-loader.html` | Small snippet pasted once into the GoHighLevel Custom Code element. It fetches `index.html` from this repo at page load. |

## Publishing
1. Edit `index.html` (products, prices, Stripe links and photos live in the `br-data` JSON block).
2. Commit to `main`.
3. Live within about 5 minutes (GitHub's raw-file cache). No GHL page-builder step.

Images and videos are still hosted in GHL Media Storage (`https://assets.cdn.filesafe.space/…`).

## Rolling back
Revert the commit (or restore an older `index.html`) and commit again.

## If the site ever shows "The site didn't load"
Both GitHub raw and jsDelivr were unreachable. Emergency fallback: paste the full `index.html` into the GHL Custom Code element (the old method) until GitHub recovers.
