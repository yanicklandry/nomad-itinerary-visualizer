# Nomad Itinerary Visualizer

Interactive visualizer for nomad itinerary route variants (V10–V28), with per-leg transport details.

## View it

GitHub Pages: https://yanicklandry.github.io/nomad-itinerary-visualizer/

## What's inside

- `index.html` — the complete visualizer (single self-contained file, no build step)
- 22 route variants, with V23 (Shanghai through-route via Laos rail) as the Base / Recommended plan
- Click any itinerary to expand transport details: date, origin/destination, mode, carrier, flight/train number, duration, cost

## Data notes

- Flight fares checked via Kiwi with 1 personal item + 1 carry-on + 1 checked bag, no US routing, max 20h elapsed. Fares are all-in totals including taxes and carrier fees.
- Rail/bus legs are estimates. Trains and buses: 20kg free allowance per adult on China and Vietnam rail (rarely enforced); no airline-style baggage fees.
- `money` figures use the nomad-cost basis for city comparison, not personal spend estimates.
- V26/V27/V28 scores are estimates computed via the delta method from V23/V24 verified scores.

## Updating

Edit `index.html` directly: route data lives in the `transportLegs` object and the `routes` array. Bump the version label when publishing changes.
