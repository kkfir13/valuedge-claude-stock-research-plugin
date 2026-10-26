---
name: valuedge-portfolio-review
description: Review the user's ValuEdge portfolio, holdings, watchlist, or Smart Alerts when they ask for read-only account analysis.
---

# ValuEdge portfolio review

Use this skill only when the user explicitly asks to analyze their own ValuEdge portfolio, holdings, watchlist, or Smart Alerts. Private account tools require the user's own ValuEdge authorization; do not ask for passwords, tokens, or another person's consent. If the connector is not connected or authorization is unavailable, explain the specific connection requirement and stop without substituting guessed holdings.

## Workflow

1. Identify the user's question and the minimum relevant account data needed. Use the live ValuEdge tool catalog and schemas; the documented read-only account tools are `get_my_portfolio`, `analyze_my_portfolio`, `get_my_watchlist`, and `get_my_smart_alerts`.
2. Retrieve only the data needed for the request. These tools read account data; do not invoke them for general market questions.
3. Summarize returned information with its as-of date, currency, source, and any missing fields or coverage limits. Distinguish the tool's reported metrics from your calculations and interpretations.
4. For concentration, exposure, or portfolio-level metrics, use `analyze_my_portfolio` when its live schema supports the requested view. Do not reconstruct unsupported metrics from incomplete holdings.
5. Treat missing, stale, or failed values as unavailable, never as zero. Do not invent holdings, prices, performance, weights, or alerts.
6. Keep the response neutral and educational. Do not make trades, modify holdings, change a watchlist, create alerts, or give buy/sell/hold instructions.

## Data minimization

Use private account data only for this user-requested response. Include only the details needed to answer; do not reproduce full account records or expose one user's data to another. ValuEdge handles account data under its [Privacy Policy](https://valuedge.app/privacy).
