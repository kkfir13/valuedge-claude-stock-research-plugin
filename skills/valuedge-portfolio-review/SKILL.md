---
name: valuedge-portfolio-review
description: Review my investment portfolio, stock holdings, diversification, concentration, allocation, portfolio risk, valuation coverage or performance context using my connected ValuEdge account.
---

# ValuEdge portfolio tracker and analysis

Use this workflow only for an explicit request about the current user's authorized ValuEdge account. Read from `get_my_portfolio` and `analyze_my_portfolio` as supported by the live tools. Private data requires the user's own OAuth authorization and applicable plan entitlement.

## Method

1. Identify the requested portfolio, date, base currency and question, relying on actual connected account data. Never infer that a displayed holding belongs to the user from a public stock question.
2. Fetch the minimum information needed. Prefer `analyze_my_portfolio` for documented concentration, allocation, value coverage and risk metrics; use holdings data only to explain or verify returned evidence.
3. Clearly distinguish a dated snapshot from live positions, and account-recorded values from independently verified market prices.
4. Identify missing or stale pricing and Fair Value coverage; do not turn absent value into a zero-value holding or calculate precise portfolio performance from incomplete data.
5. Ask before any proposed account modification; this skill itself is read-only. Do not place orders or rebalance brokerage accounts.

## Example intents

- "Analyze my portfolio concentration and largest holdings."
- "Which of my positions lack reliable fair-value coverage?"
- "Summarize my ValuEdge holdings and allocation risk."

If authorization fails, describe the ValuEdge connection requirement. Do not solicit passwords or copy another account's holdings.
