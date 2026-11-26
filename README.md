# BTC Options Lab

A single-file (no build, no dependencies) options calculator for Bitcoin options on Delta Exchange India.
Works offline for calculations; live data needs the page to be opened directly (phone browser / localhost / GitHub Pages).

## Features
- Buy/Sell calculator: current P&L, scenario P&L (BTC move % in N hours), fees, margin/exposure, max lots
- Target / SL planner, win probability, alerts (vibration + sound), liquidation estimate (Sell)
- All-moves x time grid (-12% to +12%) with BTC USD price, sparklines, tap-a-row chart
- Live BTC + option price, full option chain, "chance of going to zero" prediction tab
- Strategy builder (straddle, strangle, spreads), trade journal (stored in browser localStorage)
- English / Marathi toggle

## Install as an app (PWA)
Open the hosted page in Chrome (Android) -> menu -> *Install app* / *Add to Home screen*. On iPhone: Safari -> Share -> *Add to Home Screen*.
Files needed in the repo root: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`.

## Run
Open `index.html` in a browser, or serve it:

    python3 -m http.server 8000

## Host free on GitHub Pages
Repo -> Settings -> Pages -> Deploy from branch -> `main` / root.

## Notes
- All prices/probabilities are Black-Scholes style estimates, not predictions or financial advice.
- Delta's real margin and fees can differ from the estimates here.
- If live data fails, the browser may be blocking cross-origin requests; enter values manually.
