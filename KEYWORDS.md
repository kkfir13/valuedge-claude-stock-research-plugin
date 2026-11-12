# ValuEdge Claude Plugin — KEYWORDS / Discovery inventory

**Version:** 2026-11-12 | **MCP:** `https://valuedge.app/mcp` | **Purpose:** targeted Claude Plugin Directory discovery, not an attempt to manipulate tool selection.

## Source and limits

Reused the previously reviewed **92-term shortlist** from the Nov 10 ValuEdge ChatGPT plugin audit: **66 core** terms and **26 conditional** terms, selected out of 243 unique candidates. Unlike ChatGPT, the mechanics of Claude's directory search and ranking have not been publicly documented in enough detail to attribute ranking improvements to keyword count. `keywords` is a supported plugin manifest field for discovery tags; arbitrary extra files like this one are **not** guaranteed to affect the directory index.

**Active now:** 40 natural, capability-matched terms in `.claude-plugin/plugin.json`. **Research inventory:** all 92 here and in `KEYWORDS.json`. This is intentionally not a promise to rank first for 92 queries, and 52 candidates remain withheld until they add a demonstrable search-intent benefit.

## Active keywords in the manifest (40)

1. `ValuEdge`
2. `stock analysis`
3. `stock research`
4. `stock valuation`
5. `intrinsic value`
6. `fair value`
7. `DCF valuation`
8. `discounted cash flow`
9. `margin of safety`
10. `value investing`
11. `undervalued stocks`
12. `fundamental analysis`
13. `stock fundamentals`
14. `financial statements`
15. `cash flow analysis`
16. `valuation multiples`
17. `stock screener`
18. `stock screening`
19. `undervalued stock screener`
20. `dividend stock screener`
21. `stock comparison`
22. `compare stocks`
23. `portfolio tracker`
24. `portfolio analysis`
25. `portfolio holdings`
26. `portfolio diversification`
27. `asset allocation`
28. `stock watchlist`
29. `watchlist management`
30. `smart alerts`
31. `stock alerts`
32. `technical analysis`
33. `technical indicators`
34. `RSI`
35. `moving averages`
36. `dividend calendar`
37. `dividend tracker`
38. `ex dividend date`
39. `dividend income`
40. `portfolio transaction tracking`

## Other audited core candidates (36; not currently active)

`overvalued stocks` · `financial analysis` · `balance sheet analysis` · `earnings analysis` · `financial ratios` · `P/E ratio` · `company valuation` · `investment research` · `equity research` · `stocks` · `stock market` · `investing` · `fundamental stock screener` · `value stock screener` · `valuation screener` · `fair value screener` · `free cash flow screener` · `dividend yield screener` · `stock discovery` · `compare stock valuations` · `stock portfolio tracker` · `investment tracker` · `investment portfolio` · `stock portfolio` · `portfolio management` · `portfolio concentration` · `portfolio sector allocation` · `portfolio currency allocation` · `portfolio risk analysis` · `holdings analysis` · `watchlist` · `valuation alerts` · `fair value alerts` · `stock analysis MCP` · `stock screener MCP` · `portfolio tracker MCP`

## Conditional candidates (26; 10 active)

- `technical analysis` — active, tied to a documented MCP feature (subject to current data and account limits)
- `technical indicators` — active, tied to a documented MCP feature (subject to current data and account limits)
- `RSI` — active, tied to a documented MCP feature (subject to current data and account limits)
- `moving averages` — active, tied to a documented MCP feature (subject to current data and account limits)
- `stock momentum` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `daily technical analysis` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `SMA 20` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `SMA 50` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `SMA 200` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `dividend calendar` — active, tied to a documented MCP feature (subject to current data and account limits)
- `dividend tracker` — active, tied to a documented MCP feature (subject to current data and account limits)
- `ex dividend date` — active, tied to a documented MCP feature (subject to current data and account limits)
- `dividend payment date` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `dividend income` — active, tied to a documented MCP feature (subject to current data and account limits)
- `dividend growth` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `dividend history` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `upcoming dividend dates` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `dividend portfolio tracker` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `dividend calendar MCP` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `dividend tracker MCP` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `ETF portfolio` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `ETF analysis` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `ETF tracker` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `portfolio transaction tracking` — active, tied to a documented MCP feature (subject to current data and account limits)
- `manual portfolio tracker` — held for search evidence, more exact capability verification, or to avoid duplicative tags
- `watchlist management` — active, tied to a documented MCP feature (subject to current data and account limits)

## Intent clusters to test (not proven search volume)

| Cluster | Representative queries | Matching plugin feature |
| --- | --- | --- |
| Stock valuation | intrinsic value; DCF valuation; fair value; margin of safety | `get_stock_valuation`, valuation-review Skill |
| Screening | stock screener; undervalued stocks; dividend stock screener | `screen_stocks`, screening Skill |
| Fundamentals | fundamental analysis; stock fundamentals; financial statements | `get_stock_fundamentals` |
| Comparisons | compare stocks; stock comparison | `compare_stocks` |
| Technicals | RSI; moving averages; technical analysis | `get_stock_technicals`; **daily** historical readings, not intraday |
| Portfolio | portfolio tracker; portfolio analysis; asset allocation | `get_my_portfolio`, `analyze_my_portfolio`, with OAuth |
| Watchlists and alerts | stock watchlist; smart alerts; stock alerts | Watchlist/Smart Alerts user-scoped tools |
| Dividends | dividend tracker; dividend calendar; ex dividend date | `get_my_dividend_tracker`, `get_dividend_calendar` |
| Account record maintenance | portfolio transaction tracking; watchlist management | Explicitly confirmed user-requested account edits; no broker orders |

## Excluded or unverified claims

Do not use competitor trademarks as keywords. Do not market live trading, intraday signals, brokerage execution, automated investing, guaranteed returns, ETF-specific research without a directly supported tool, market-wide exhaustive screening, or website-only Backtesting as MCP capabilities.

## What changes visibility

1. `.claude-plugin/plugin.json` `displayName`, `description`, `keywords` are the submission's declared discovery metadata.
2. Skill names and their frontmatter descriptions accurately communicate invocation intent; there is no published guarantee they directly influence directory rankings.
3. Directory entry copy, category if offered, examples and screenshots should be truthful, concise and focused on first value.
4. After publication, measure **actual search terms leading to listing views**, then installs and first useful tool calls. Prefer changing one listing variable per review cycle.

See `DISCOVERY-PLAN.md` and `STARTER-PROMPTS.md` for experiments and examples.
