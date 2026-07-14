# TradeForge — Trading Strategy App

## Status

Idea — not started. Details to be filled in with Juan (existing Pine Script work referenced
but not yet described here).

## Problem Statement

Build an app around existing trading-strategy logic (previously written in Pine Script for
TradingView) — scope, target platform, and whether it stays on TradingView vs. becomes a
standalone app are still open.

## Open Questions

- What does the existing Pine Script strategy do, and does it need to be ported (e.g. to
  Python) or just wrapped/automated?
- Standalone app, broker API integration, or TradingView-hosted? Live trading, paper trading,
  or backtesting only?
- Data source and hosting: local script vs. cloud-deployed service?

## Roadmap Connections

Good capstone-style candidate for Phase 2 (Python), Phase 5 (cloud hosting), Phase 6
(containerizing the app), Phase 7 (IaC for its infrastructure), and Phase 10 (monitoring a
live trading service) — once the foundations are far enough along.

## Next Steps

- Write down what the current Pine Script strategy actually does, in plain language.
- Decide the smallest useful first version (e.g. a backtester) before scoping the full app.
