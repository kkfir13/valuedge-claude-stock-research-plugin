---
name: valuedge-valuation-review
description: Review ValuEdge valuation and fundamentals for public companies, or compare two to six securities, when the user asks for stock research.
---

# ValuEdge valuation and fundamentals review

Use this skill for public-company research using ValuEdge's read-only tools. The documented tools are `search_securities`, `get_stock_valuation`, `get_stock_fundamentals`, and `compare_stocks`; comparisons support two to six tickers. Inspect the live tool catalog and schemas before calling them.

## Workflow

1. Resolve the company and listing. If a name, ticker, exchange, or share class is ambiguous, use `search_securities`; show plausible matches and ask the user to choose before calling issuer-specific tools.
2. Call only the tool(s) needed for the question. Use `get_stock_valuation` for ValuEdge's returned valuation view, `get_stock_fundamentals` for returned financial data, and `compare_stocks` for an explicitly requested comparison of two to six tickers.
3. Present reported fields as ValuEdge results. Preserve valuation method, assumptions, periods, currency, timestamps, and confidence or coverage metadata when returned. Clearly label any arithmetic or interpretation you add.
4. Explain material missing, stale, or inconsistent inputs. Do not fill gaps with fabricated forecasts, prices, multiples, or a precise fair value. If a result lacks enough detail for a conclusion, say what is missing.
5. Keep conclusions descriptive and balanced. Do not promise returns or accuracy, provide buy/sell/hold instructions, or imply a valuation is a guaranteed future price.

If a tool is disconnected, denied, or fails, name the unavailable result and stop short of a ValuEdge-backed conclusion. Do not reinterpret an error as zero or as proof that a security is unsupported.
