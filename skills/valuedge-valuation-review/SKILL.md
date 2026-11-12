---
name: valuedge-valuation-review
description: Analyze stock valuation, intrinsic value, fair value, DCF assumptions, margin of safety, financial statements, fundamentals or compare stocks with ValuEdge when the user asks for evidence-based equity research.
---

# ValuEdge stock valuation and fundamental analysis

Use the existing ValuEdge MCP tools `search_securities`, `get_stock_valuation`, `get_stock_fundamentals` and `compare_stocks` as the live catalog permits.

## Method

1. Resolve ambiguous issuer, ticker, exchange, security type or share class with `search_securities` before requesting financials. Never silently switch listings.
2. Use the minimum required tool calls. For an intrinsic-value or DCF question use `get_stock_valuation`; for financial health use `get_stock_fundamentals`; for side-by-side research use `compare_stocks` when its live inputs support the requested securities.
3. Present ValuEdge's returned Fair Value, margin of safety, growth, profitability, multiples, periods, calculation basis, risks and dates only when actually supplied. Distinguish model output from a market quote and from your interpretation.
4. Carry through valuation withholding, missing data, source limitations and data freshness. Never invent DCF assumptions, earnings, a valuation number, or a valuation model version; never substitute unavailable values with zero.
5. Account entitlements and research quotas differ by tool. Follow an OAuth challenge or plan-limit explanation as returned; do not work around limits or promise free unlimited analysis.

## Example intents

- "What's the ValuEdge fair value and margin of safety of AAPL?"
- "Explain MSFT's financial fundamentals and the assumptions behind its valuation."
- "Compare GOOGL and META using their available valuation and balance-sheet evidence."

Research only; no recommendation to buy or sell and no future-return guarantee.
