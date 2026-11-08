# DOGE strategy board

Live one-card trading instruction for DOGE-USDT-SWAP (4H channel breakout + EMA200 filter).

Single static page: computes EMA / ATR / RSI / 20-bar channel in the browser from OKX public
market data, refreshes every 30 seconds, no backend, no keys.

Rules
- 4H close above EMA200 -> long only; below -> short only.
- Long when the 4H close takes out the prior 20-bar high; short when it loses the prior 20-bar low.
- Stop 2 x ATR(4H) beyond entry, target 3R.
- Size = equity x 3% / stop distance; leverage picked so the liquidation price sits at least 3x the stop distance away (max 10x).

Not financial advice.
