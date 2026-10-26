---
name: valuedge-stock-screening
description: Screen supported public stocks with ValuEdge when the user asks for candidate discovery or a focused stock screen.
---

# ValuEdge stock screening

Use the ValuEdge screener for a bounded search of supported public securities. The documented universe is NYSE- and NASDAQ-listed securities. ValuEdge documents a candidate window of up to 60 and no more than 12 returned results; do not describe results as exhaustive or as the whole market.

## Workflow

1. Translate the user's request into explicit, supported filters. Ask a concise follow-up only when a missing choice would materially change the screen.
2. Inspect the live MCP catalog and `screen_stocks` schema. Use only available presets and parameters; never invent preset IDs, filters, exchanges, or output fields.
3. Keep result limits within the documented maximum and candidate window. If the live schema or result indicates different current limits, report what the live response actually supports.
4. Present candidates as a starting point for research, with the filters, date or freshness information returned, and any coverage caveats. Explain when a filter could not be applied.
5. Do not rank a candidate as universally best, infer unsupported investment conclusions, or tell the user to buy, sell, or trade.

If the screener is unavailable, fails, or returns no rows, state that plainly. A failed request is not evidence that no securities meet the criteria.
