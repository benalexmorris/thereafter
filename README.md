# Thereafter

Wedding fragrance sold as a package, not a bottle. Eight pre-composed fragrances,
each named for the number of raw materials in it. Three tiers. Free samples posted.
No appointment in London.

## Running it

A single self-contained `index.html` — inline CSS and JS, no build step, no
dependencies beyond Google Fonts. Open the file in a browser, or serve the folder:

```bash
python3 -m http.server 4173
```

## Structure

All content lives in three plain arrays near the top of the `<script>` block:

| Array | Holds |
| --- | --- |
| `FRAGRANCES` | id, display name, raw-material count, feel, season, hue, chip words, quote, notes |
| `TIERS` | numeral, name, price, what it includes |
| `STRENGTHS` | label and explanatory note for the per-fragrance dial |

`BOTANICAL` holds one hand-drawn SVG line illustration per fragrance.
`REEL` maps one hero clip URL per fragrance id and is empty by default — the
colour wash carries the hero on its own, and the site is finished with zero video.

Nothing needs a CMS yet.

## Known open items

The material counts (12, 18, 9, 24, 16, 31, 7, 29) are placeholders chosen to feel
plausible. They appear in the display name, the card corner, the spec table and the
batch line, and are derived from a single `n` per fragrance — correct `n` and every
occurrence follows. The whole device depends on the number being true.

The "naturally derived" and "pet-safe formulations" claims in the credentials row
need a perfumer's sign-off before this goes near a customer.

## Out of scope

Checkout and payments, accounts, a CMS, real email or calendar integration, the
recommendation model itself, multi-page routing, and the video assets.
