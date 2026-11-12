---
name: valuedge-watchlist-management
description: Read, organize or manage my ValuEdge stock watchlist, watchlist folders, tracked stocks and Smart Alerts when I explicitly request actions on my connected account.
---

# ValuEdge watchlist tracker and management

For read-only requests use `get_my_watchlist`, `list_my_watchlists` and `get_my_smart_alerts` when present. For user-requested account changes the main ValuEdge MCP may expose `add_to_my_watchlist`, `remove_from_my_watchlist`, `create_my_watchlist` and `rename_my_watchlist`. Always check actual live catalog, OAuth identity, permissions and plan quotas.

## Method

1. Determine whether the user asks to **inspect** or **change** their watchlist. Never modify anything in response to a vague research question.
2. For inspection, retrieve the minimum relevant account data and note valuation coverage, stale fields, folder membership and account limits.
3. For changes, confirm the exact ticker, destination watchlist/folder and requested operation with the user before calling a mutating tool. In particular, obtain explicit confirmation before removal or a change that affects more than one entry.
4. Call only the specified write tool with authorized account identity. Never bypass quota/permissions or claim completion until the tool confirms the change.
5. Where a tool is absent or denied, explain the requirement and offer a read-only alternative.

Examples:
- "Show the stocks in my ValuEdge watchlist."
- "Add MSFT to my ValuEdge watchlist." (confirm destination/intent before the change)
- "Which of my saved stocks have a Smart Alert?"

The connector does not place brokerage trades; watchlist editing is not order execution.
