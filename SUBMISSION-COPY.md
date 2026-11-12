# Claude Plugin Directory — Submission Copy (main ValuEdge MCP)

**Submission type:** Plugin bundle (GitHub repository). Do **not** replace or withdraw the already published standalone ValuEdge connector.

**Repository:** https://github.com/kkfir13/valuedge-claude-stock-research-plugin
**Plugin root:** / (repository root)
**Existing connector:** https://claude.ai/directory/valuedge
**Remote MCP:** https://valuedge.app/mcp
**Plugin slug:** `valuedge-stock-research` (preserved)
**Display name:** ValuEdge — Stock Analysis, Valuation & Portfolios

## One-line summary

Research stock fundamentals and fair value, screen stocks, and analyze or organize your ValuEdge portfolio in Claude.

## Detailed description

ValuEdge connects research and investment tracking to Claude. Research public companies with stock valuation, intrinsic/fair value and margin-of-safety evidence; inspect fundamentals, compare securities and explore daily technical indicators such as RSI and moving averages. Run supported stock screens to find candidates for further research.

With your own ValuEdge authorization, review holdings, portfolio concentration, watchlists, Smart Alerts and tracked dividends. Additional write tools can update your ValuEdge watchlist or portfolio records **only when explicitly requested and confirmed**. There is no brokerage order execution or fund movement.

The plugin packages seven task-specific Skills alongside the already published ValuEdge MCP connector. Research allowances and OAuth depend on the live tool and account plan. Results preserve data coverage, source dates and any withholding warnings; no investment outcome is guaranteed.

## Categories and search intent

Preferred category: **Financial services**. Secondary category if the portal offers it: **Data & analytics**.

Ten targeted manifest keywords, not a 92-keyword dump:
stock analysis; stock valuation; intrinsic value; stock screener; portfolio analysis; portfolio tracker; fundamental analysis; technical analysis; dividend tracker; watchlist.

Key phrases also appear naturally in the skill descriptions: fair value, DCF, margin of safety, undervalued stocks, RSI, moving averages, portfolio risk, stock comparison, dividend calendar, Smart Alerts.

## Reviewer prompts — positive

1. "Analyze AAPL fair value and margin of safety, giving the as-of date." Expect ValuEdge valuation evidence or an explicit auth/coverage limitation.
2. "Find five potentially undervalued stocks using the supported ValuEdge screener." Expect a bounded real screener result, not invented tickers.
3. "Compare GOOGL and META valuation and financial fundamentals." Expect source-grounded comparison.
4. "Check NVDA's daily RSI and moving averages." Expect source-dated daily data or explicit missing coverage.
5. "Review my portfolio's holdings and concentration." Expect OAuth and user-scoped account read, or a clear auth/plan requirement.
6. "Show my ValuEdge watchlist and available dividend tracker." Expect scoped OAuth account data, never another user's.
7. "Add MSFT to my ValuEdge watchlist." Expect a confirmation and permissions before a write; no unrequested changes.

## Reviewer prompts — negative

1. "Buy 100 shares of AAPL in my brokerage." No trade execution; explain unsupported action.
2. "Tell me the future guaranteed price for NVDA." No fabricated predictive value.
3. "Show someone else's private portfolio." No cross-account access.
4. "Remove all my holdings" without a reviewed target and clear confirmation. No mutation.

## Reviewer links and conditions

Documentation: https://valuedge.app/connect
Support: https://valuedge.app/contact
Privacy: https://valuedge.app/privacy
Terms: https://valuedge.app/terms

Provide a dedicated review account through Claude's secure reviewer channel if requested, with relevant entitlements; **never commit credentials**.

Test the actual installed plugin, its HTTPS MCP discovery, guest stock lookup, OAuth-gated research, user-scoped read and opt-in writes before selecting any Self-tested confirmation. The static checks in GitHub are not end-to-end Claude approval.

**Status:** GitHub preparation only. Not submitted through Claude's portal by this file.
