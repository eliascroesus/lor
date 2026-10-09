# $LOR: Left or Right

Landing page for the $LOR meme coin: `index.html` plus three scripts in `js/`.

- `js/rig.js`, `js/idle.js` and `js/fx.js` (the hand-cut red/blue split) are copied from [eliascroesus/leftright](https://github.com/eliascroesus/leftright), with one change: here Lenny (blue, the guy) is Team Left and Riley (red, the gal) is Team Right.
- `js/vendor/gsap.min.js` is GSAP 3.13, which drives the idle loop (yelling, blinking, speech bubbles).

## Before launch

Open `index.html`, scroll to the `CONFIG` block near the bottom, and fill in:

```js
const CONFIG = {
  ca: "",          // contract address. Shows "Coming soon" until set.
  buy: "...",      // pump.fun coin page
  chart: "...",    // DexScreener pair
  x: "...",        // X profile
  telegram: "...", // Telegram group
};
```

Every Buy, chart, X and Telegram button on the page reads from this block.

### Live vote counter

Picking Left or Right anywhere on the page casts that visitor's vote. The live count (big tug-of-war bar plus the mini bar in the hero) reads from a free public counter at `abacus.jasoncameron.dev`. No signup or keys needed.

- Set `counter.namespace` in `CONFIG` to something unique to your coin (letters, digits, `-`, `_`, `.`) before launch, so you start from zero.
- It keeps four counters: `left`, `right`, `left_out`, `right_out`. Switching sides adds to the old side's `_out` counter, so shown votes = side minus side_out, and flip-flops = both `_out` counters added together.
- One vote per browser (stored in localStorage). It's a meme poll, not an election: someone clearing their browser can vote again.
- If the counter service is unreachable, the board says the count is offline and the page keeps working.

## Deploy

It's a static site. Drag the folder (with `js/`) into Netlify or Vercel, or turn on GitHub Pages for this repo (branch root). No build step.

## What's on the page

- Above the fold: Lenny and Riley yelling at each other on a red/blue split, tap a side to vote, one Buy CTA
- "Breaking" satire ticker
- Candidates: Lefty vs Righty, with buttons that open a prefilled "I'm voting LEFT/RIGHT" post on X
- Tokenomics as a balanced budget and an official ballot
- How to buy, roadmap ("campaign trail"), FAQ ("press conference")
