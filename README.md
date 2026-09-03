# mint-sanity
 
A one-page public lookup: paste a Solana token mint, fetch [DexScreener](https://api.dexscreener.com/latest/dex/tokens/{mint}), and show name, symbol, liquidity USD, 24h volume, pair created time, and a plain tag (`thin` / `ok` / `unknown`). No keys. No trading advice.

**Why this exists.** Most mint checks dump you into a chart or a wallet prompt. This page only repeats public pair stats so you can see whether DexScreener knows the mint at all.

Tag rule, using the highest-liquidity pair: `unknown` if there is no pair or no USD liquidity; `thin` if liquidity is under $10,000; `ok` otherwise. That is a liquidity snapshot, not a recommendation.

A written custom report for one mint is **$5**. Open a GitHub issue at https://github.com/louist369/mint-sanity/issues to request it.

## Run locally

Open `index.html` in a browser, or from this directory:

```bash
python3 -m http.server 43127
```

Then visit `http://127.0.0.1:43127`.

MIT licensed. Data comes from DexScreener and can be wrong, stale, or missing.
