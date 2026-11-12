---
name: valuedge-stock-screening
description: Use ValuEdge's stock screener when the user wants to find undervalued stocks, search by margin of safety, screen dividend or quality stocks, or shortlist equities using specific supported filters.
---

# Stock screening with ValuEdge

Use `screen_stocks` from the existing ValuEdge MCP connection when a user asks for candidate discovery or a stock screen. The endpoint is `https://valuedge.app/mcp`; never create a second account or request credentials.

## Method

1. Translate the request into the **live** tool's supported filters, presets, ranking, and result limits. Do not invent schema fields, filters, available exchanges, or universes. If a requested condition is unsupported, disclose the limitation.
2. Use one appropriately bounded `screen_stocks` call first; follow with more precise research only when needed. Respect the user's ValuEdge account limits and OAuth requirements when returned.
3. Label results as ValuEdge-sourced research candidates, not an exhaustive scan or investment recommendations. State applied filters, coverage, valuation freshness and data gaps, where supplied.
4. When Fair Value, intrinsic value, or margin of safety is unavailable or withheld, omit the numerical claim rather than substituting a stale or speculative value.
5. If a request fails, times out or returns no matches, distinguish **technical failure** from **valid zero matches** and offer a narrower supported screen or a retry. Never invent matches.

## Example intents

- "Find undervalued stocks with a positive margin of safety."
- "Screen companies with positive free cash flow."
- "Show dividend stocks that meet my filters."

Never promise a market-wide ranking, guaranteed returns, or real-time coverage. Do not trade or change a user's account while screening.
