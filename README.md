# Nomad Itinerary Visualizer

Interactive month-by-month comparison of every nomad itinerary variant for Oct 2026 to Oct 2027, with per-leg transport details.

## View it

GitHub Pages: https://yanicklandry.github.io/nomad-itinerary-visualizer/

## What's inside

- `index.html`: the whole visualizer (one self-contained file, no build step).
- 51 routes in three groups:
  - **With the Shanghai week** (Gabryl, Dec 6 to 13): V23 (base plan chosen Oct 13), V23b to V41 (V38: current front end, Oct 14). Comparable with each other.
  - **Without the Shanghai week** (Oct 8 to 12): V8 to V22, V14b, S0, W1, W4, BR2.
  - **Early drafts** (Oct 7 rules, not comparable): Route A, Spines, V3 to V7, the Dream Trip plan.
- Controls: weight profile (Default, Friends first, Weather first, Discovery first) and the value of one point (CAD 300, 1,000, 3,000). The ranking and the takeaway update live.
- Each row shows score, money, transport, cold and wet nights, the change against the base plan, and chips for what matters (Shanghai with Gabryl, Seoul with Mikael, Melbourne with Tony, Singapore, Madrid, a return to Vietnam, a Thai e-visa need).
- Click a row for its transport legs: date, from/to, mode, carrier, flight or train number, duration, cost and notes.

## Data notes

- Scores use the Nomad Planner method (Notion, section 2). Rows from Oct 12 onward were rescored together by Claude on Oct 14 with the 1-month Sao Paulo tail (Lima to Sep 20); differences against Muse's published values are 0.4 points or less, except the delta-method estimates for V26 to V28, which were replaced by full scores.
- Flight fares: Kiwi, 1 personal item + carry-on + checked bag, no US routing, 20h cap, all-in prices. Rail and bus legs are estimates.
- `money` uses the nomad-cost basis for comparing cities, not a personal budget.
- Thailand: 30-day visa exemption for Canadians since Sep 15, 2026, extendable once by 30 days. Laos: e-visa required for the Boten rail border. China: 30 days visa-free for Canadians until at least Dec 31, 2026.

## Updating

Edit `index.html`: route data is the `ROWS` array (blocks are `[city, start, end]`, end = departure day) and transport legs are the `transportLegs` object. Bump the version label when publishing.
