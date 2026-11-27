# BTC Options Lab V6 Pro

A client-side BTC options research dashboard upgraded from V5. No build step.

## V6 additions
- Expiry-scoped OI strike heatmap and IV skew view using the selected Delta India options chain.
- Liquidity proxy ranked from available OI, volume and quoted bid/ask spread (not order-book depth).
- Illustrative leverage bands (not exchange liquidation prices).
- Bull call spread, bear put spread and iron condor candidate builder; requires valid quotes and labels estimates/limitations.
- EMA crossover BTC spot-proxy backtest on locally saved candles, with next-candle-open fills and configurable estimated per-side cost. This is not an options strategy backtest.
- Browser-local price, IV and OI alerts; checks occur when the app refreshes/renders and are not guaranteed background/push alerts.
- Open paper-trade risk summary with Delta only where recorded, plus closed-journal analytics.
- Public market-data fetch buttons for Delta India, Deribit BTC options summary and Binance BTC spot.

## Retained V5 features
Calculator, Black-Scholes estimates, Greeks, option chain, expiry scanner, strategy builder, paper trading, journal, charts, CSV export, Marathi/English UI, local persistence and PWA support.

## Run
Open `index.html` or serve the folder with `python3 -m http.server 8000`. Deploy all files to the GitHub Pages repository root.

## Data and risk limitations
- This is an analysis/research tool, not an execution terminal and not investment advice. No orders or private exchange endpoints are used.
- Public APIs may fail due to CORS, network, regional access or exchange changes. Multi-exchange responses are displayed independently and are not normalized into one comparable option chain.
- OI/IV values are only as reliable as the source chain snapshot. Liquidity score is a proxy, not market depth. The leverage bands are illustrative, not liquidation predictions.
- Strategy builder estimates exclude fees, slippage, margin, exercise/settlement details and early exit effects. Verify contract multiplier and quote currency with the exchange.
- Backtest is long-only BTC spot proxy using local candles; it does not simulate BTC options, funding, taxes, market impact or guaranteed fills.
- Smart alerts are browser-local and require the app to be open/refreshed; no server-side or guaranteed background notifications.
- All model probabilities, Greeks, margin and P&L are estimates. Confirm current exchange specifications before any trade.
- Existing V4/V5 localStorage keys are preserved; V6 service worker cache is namespaced separately.

## Validation
Syntax, duplicate HTML IDs, ZIP integrity and targeted calculator/backtest edge cases are checked in the build environment. Live exchange availability must be verified on the user's device/network.
