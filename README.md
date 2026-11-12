# ValuEdge — Stock Analysis, Valuation & Portfolios for Claude

A user-installable Claude plugin for **stock analysis, stock screening, intrinsic-value research, daily technical indicators, and authorized portfolio management**. This plugin adds focused Claude Skills to ValuEdge's existing, publicly listed remote MCP connector.

- Official ValuEdge MCP endpoint: **https://valuedge.app/mcp**
- Existing Claude connector: **https://claude.ai/directory/valuedge**
- Documentation and ValuEdge account connection: **https://valuedge.app/connect**

## What you can ask

| Intent | Example | Skills / MCP tools |
| --- | --- | --- |
| Stock analysis and intrinsic value | "Analyze AAPL fair value, margin of safety, and key assumptions." | `valuedge-valuation-review`; `get_stock_valuation`, `get_stock_fundamentals` |
| Stock screener | "Find undervalued stocks with a positive margin of safety." | `valuedge-stock-screening`; `screen_stocks` |
| Stock comparisons | "Compare GOOGL and MSFT fundamentals and valuations." | `valuedge-valuation-review`; `compare_stocks` |
| Technical analysis | "Check NVDA's daily RSI, moving averages and trend." | `valuedge-technical-analysis`; `get_stock_technicals` |
| Portfolio tracker | "Review my holdings and concentration risk." | `valuedge-portfolio-review`; `get_my_portfolio`, `analyze_my_portfolio` |
| Watchlist and alerts | "Show my saved stocks and Smart Alerts." | `valuedge-watchlist-management`; watchlist and alert tools |
| Dividend tracker | "Show my tracked dividends and the dividend calendar." | `valuedge-dividend-research`; `get_dividend_calendar`, `get_my_dividend_tracker` |
| Portfolio records | "Correct an entry in my portfolio transaction history." | `valuedge-portfolio-transactions`; authorized record-write tools |

**Coverage is conditional.** Check each tool's current schema, authorization requirements, account quotas and data coverage. ValuEdge may withhold incomplete valuations or unsupported market data. Daily technical signals are not live intraday quotes.

## Connect in Claude

1. Install the plugin from its approved directory listing when published, or load this repository as a developer plugin for testing.
2. Connect the existing **ValuEdge — Stock Research & Portfolio Analysis** remote connector when prompted. Both point to `https://valuedge.app/mcp`; this repository does not create a new MCP server.
3. Sign in to your own ValuEdge account using the normal OAuth flow **only** when using account-scoped or metered research tools. An eligible plan and available research allowance may be required. Do not share API keys or passwords.
4. Ask natural-language research questions or invoke one of the seven skills.

## Read/write boundary

Stock research is analytical. Some account tools can **change watchlist folders, tracked symbols or portfolio transaction records** only after the user explicitly requests and confirms the relevant action, subject to OAuth and plan restrictions. The integration does **not** place brokerage trades, send orders, move money or rebalance a brokerage account.

No tokens, passwords, user data, remote scripts or install-time dependencies are bundled. The plugin references one HTTPS MCP endpoint.

## Evidence and privacy

Data is returned from ValuEdge as available; display source dates, warning/withholding reasons and coverage limits. A failed tool call is not a zero or an unsupported ticker. For collection, processing and retention consult [ValuEdge Privacy](https://valuedge.app/privacy) and [Terms](https://valuedge.app/terms).

## Directory submission

Submission copy, keyword clusters and reviewer smoke tests are in [SUBMISSION-COPY.md](SUBMISSION-COPY.md), [DISCOVERY-PLAN.md](DISCOVERY-PLAN.md) and [REVIEW-TESTS.md](REVIEW-TESTS.md).

**This GitHub repository being public does not mean the Claude plugin is approved or published.** The directory submission portal must validate and approve it separately.

MIT covers original plugin instructions and docs only; ValuEdge brand assets and third-party data retain their own rights.
