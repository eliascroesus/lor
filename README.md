# $LOR: Left or Right

Landing page for the $LOR meme coin. One self-contained file: `index.html` (HTML, CSS and JS inline, fonts from Google Fonts).

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

## Deploy

It's a static file. Drag the folder into Netlify or Vercel, or turn on GitHub Pages for this repo (branch root). No build step.

## What's on the page

- Hero with a 3D coin you can toss (LEFT or RIGHT) and parody campaign pins
- "Breaking" satire ticker
- Candidates: Lefty vs Righty, with buttons that open a prefilled "I'm voting LEFT/RIGHT" post on X
- Tokenomics as a balanced budget and an official ballot
- How to buy, roadmap ("campaign trail"), FAQ ("press conference")
