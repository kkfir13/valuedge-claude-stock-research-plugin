---
name: valuedge-technical-analysis
description: Check daily stock technical analysis in ValuEdge for RSI, SMA20, SMA50, SMA200, trend, momentum, volume or moving-average signals when the user asks for technical indicators on a particular stock.
---

# Daily stock technical analysis

Use `get_stock_technicals` on the **main** ValuEdge MCP when the request concerns daily technical indicators for a resolved stock, and the current catalog exposes that tool.

## Method

1. Resolve an ambiguous ticker with `search_securities`, then use the technicals tool. Inspect actual inputs and scope; do not invent timeframes or parameters.
2. Explain any returned RSI, SMA20/50/200, momentum, volume, trend or other indicators using the dates and sources actually present in the response.
3. Label readings as daily / historical as appropriate. Do not portray them as intraday, tick-level, live trading signals or guaranteed price forecasts.
4. If data is missing, unsupported or stale, state that specifically. Do not fabricate an indicator, a support level, or a crossover.
5. Avoid invoking a Backtesting Expert or simulated strategy tool unless it actually appears in the live MCP catalog; website-only features are not automatically MCP capabilities.

Example: "What do NVDA's ValuEdge daily RSI, moving averages and trend data currently show?"

This skill supplies descriptive research, not trading execution or personalized financial advice.
