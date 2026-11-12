---
name: valuedge-dividend-research
description: Research a stock's dividend calendar, ex-dividend or payment dates, historical dividends, and review my own ValuEdge dividend tracker when I request dividend income or cash-flow tracking.
---

# Dividend calendar and tracker

Use `get_dividend_calendar` for supported public dividend-history or dividend-event questions; use `get_my_dividend_tracker` only after the user's own ValuEdge OAuth authorization and only for their account. Confirm that each tool exists in the live catalog.

## Method

1. Resolve the security first if ticker or listing is ambiguous.
2. For public companies, retrieve the reported dividend calendar and identify whether dates are past, announced future events, or absent. Do not infer unannounced future dividends from a historical payment pattern.
3. For portfolio dividend questions, load only the user's authorized tracker data and keep income, frequency and currency grounded in the returned tool response.
4. Disclose source dates, currency and coverage. Never invent dividend rates, payment amounts or declared dates.
5. Never modify account records or schedule trades in response to a research question.

Example: "Show KO's dividend calendar and explain which future payments, if any, are confirmed."
Example: "Review the dividends available in my ValuEdge tracker."
