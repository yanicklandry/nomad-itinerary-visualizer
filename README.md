# Nomad Itinerary Visualizer

Interactive month-by-month comparison of every nomad itinerary variant for Oct 2026 to Oct 2027, with per-leg transport details.

## View it

GitHub Pages: https://yanicklandry.github.io/nomad-itinerary-visualizer/

## What's inside

- `index.html`: the whole visualizer (one self-contained file, no build step).
- 56 routes in five groups:
  - **Current choices, with the Shanghai week** (Oct 18): V38 (Action plan), V39 to V42w. All start Hanoi Oct 26 to Nov 1 with no 33h train. Best: V42 (Da Nang in February).
  - **Current choices, without the Shanghai week** (Oct 18): V43 to V45. Best: V44 (Da Nang in January).
  - **With the Shanghai week, Oct 13 to 14 drafts**: V23 (base plan chosen Oct 13), V23b to V35. Built on the 33h train rejected Oct 14.
  - **Without the Shanghai week** (Oct 8 to 12): V8 to V22, V14b, S0, W1, W4, BR2.
  - **Early drafts** (Oct 7 rules, not comparable): Route A, Spines, V3 to V7, the Dream Trip plan.
- Controls: weight profile (Default, Friends first, Weather first, Discovery first) and the value of one point (CAD 300, 1,000, 3,000). The ranking and the takeaway update live.
- Each row shows score, money, transport, cold and wet nights, the change against the base plan, and chips for what matters (Shanghai with Gabryl, Seoul with Mikael, Melbourne with Tony, Singapore, Madrid, a return to Vietnam, a Thai e-visa need).
- Click a row for its transport legs: date, from/to, mode, carrier, flight or train number, duration, cost and notes.

## Data notes

- Since Oct 18, rows in the current-choice groups without Da Nang carry the G3 must-have penalty (-10). Published scores use Bali internet = 2 (the Notion data page says 3); this lowers every row by about 0.3 and does not change any ranking.

- Scores use the Nomad Planner method (Notion, section 2). Rows from Oct 12 onward were rescored together by Claude on Oct 14 with the 1-month Sao Paulo tail (Lima to Sep 20); differences against Muse's published values are 0.4 points or less, except the delta-method estimates for V26 to V28, which were replaced by full scores.
- Flight fares: Kiwi, 1 personal item + carry-on + checked bag, no US routing, 20h cap, all-in prices. Rail and bus legs are estimates.
- `money` uses the nomad-cost basis for comparing cities, not a personal budget.
- Thailand: 30-day visa exemption for Canadians since Sep 15, 2026, extendable once by 30 days. Laos: e-visa required for the Boten rail border. China: 30 days visa-free for Canadians until at least Dec 31, 2026.

## Updating

Edit `index.html`: route data is the `ROWS` array (blocks are `[city, start, end]`, end = departure day) and transport legs are the `transportLegs` object. Bump the version label when publishing.
