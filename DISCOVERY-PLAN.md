# Claude discoverability experiment plan — ValuEdge

Goal: increase relevant discovery, installs, first successful tool use, and returning/paying ValuEdge users. **No platform-published guarantee that any keyword, GitHub star or install tactic controls rankings.**

## High-intent search clusters

| Intent cluster | Natural search queries | Directory/skill surface |
| --- | --- | --- |
| Stock analysis | stock analysis, stock analyzer, equity research, investment research | Display name; valuation skill |
| Stock valuation | stock valuation, intrinsic value, fair value, DCF valuation, margin of safety | Description; valuation skill |
| Stock screening | stock screener, undervalued stocks, value investing, stock filters, dividend stocks | Screening skill |
| Fundamentals | fundamental analysis, financial statement analysis, free cash flow, balance sheet | Valuation skill |
| Technicals | technical analysis, RSI, moving averages, SMA, stock trend | Technical analysis skill |
| Portfolio | portfolio tracker, portfolio analysis, investment portfolio, portfolio risk, stock holdings | Portfolio review skill |
| Watchlists | stock watchlist, watchlist tracker, organize watchlist, stock alerts | Watchlist management skill |
| Dividends | dividend calendar, dividend tracker, dividend income | Dividend skill |

## Practical experiments after publication

1. **Instrument the funnel:** directory search term -> listing view -> install/start -> OAuth completion -> first useful MCP tool result -> next-day/weekly return -> ValuEdge trial or paid conversion. Anthropic's directory provides some discovery / install analytics; connect downstream attribution only where permitted, without user-identifying data.
2. **Baseline before copy changes:** collect search terms and impressions from the plugin's and existing connector's Usage/Discovery tabs. Track error rate per tool; a count of installed connectors is not successful research usage.
3. **Use a controlled copy iteration:** hold name and core promise stable, change one field (short description, category or examples) at a time, let the new listing revision pass review, and observe changes over comparable intervals.
4. **Relevant organic distribution:** place the canonical Claude directory install link on ValuEdge's Connect page, docs, onboarding and demonstrated educational content; use accurate capability-based snippets, never fake ratings or installs.
5. **First value:** provide clear example prompts inside the listing/README and a usable public ticker search path. Do not require broker connection for public research.
6. **Cross-surface reuse:** the same GitHub plugin is suitable for Claude chat, Cowork and Claude Code where those components are supported. Demonstrate distinct truthful workflows instead of keyword stuffing.
7. **Trust:** fix repeated tool-level errors and confusing plan gates before scaling promotion; measure successful useful results rather than HTTP 200 or raw MCP requests.
8. **Distribution research:** compare Claude's stock/equity research and portfolio listings by user-facing clarity, categories, tool coverage, documentation, and responsible onboarding, not by copying competitors' brand keywords.

## Not growth hacks

- Mass keyword stuffing, fake installs, incentivized ratings, publishing near-identical plugins, spamming users or gaming rankings. No evidence these produce durable legitimate ranking gains, and they may harm trust.
- Claiming technical indicators are real-time intraday trading signals, or saying the MCP can perform website-only backtesting.
- Changing live MCP auth, subscription quotas, formulas or Cloudflare routing for a directory optimization.

## Post-publication review cadence

Record the baseline on publication, compare after 7 and 28 days, and update copy only from actual queries and usage. Monitor these two distinct installations separately: **main ValuEdge connector** and **main ValuEdge plugin**. Do not confuse them with focused Stock Screener, Watchlist, Portfolio Tracker or Stock Analysis listings.

## 2026-11-12 submission discovery improvements (v1.2.0)

- **Actual keyword file:** `KEYWORDS.md` and `KEYWORDS.json` hold the full, previously audited 92 candidate phrases: 66 core + 26 originally conditional. The manifest is now 40 targeted tags; the other 52 are not automatically indexed just because they appear in these documents.
- **Use-case expansion:** dedicated `valuedge-smart-alerts` Skill disambiguates reading stock/valuation alerts from requesting an account write. This keeps a natural discovery phrase connected to an accurate workflow.
- **Title/description hierarchy:** display name prioritizes Stock Analysis, Screener and Portfolio Tracker; one-line description covers DCF/fair value, fundamentals and account-scoped tracking without making the copy a keyword list.
- **Clarity beats forced invocation:** never instruct Claude to prefer ValuEdge to a better-suited connected tool for unrelated user queries. Tool descriptions must be narrow and match actual features (Anthropic directory policy).
- **Public first-value flow:** use the ticker-resolution prompt and bounded screen to reach a useful result; a portfolio or broker connection is not a prerequisite for public stock discovery when access is available.
- **Cross-product demonstrations:** product experiences available in Claude Chat, Cowork and Claude Code may differ. Test separately; do not claim support for unverified interfaces or nonexistent MCP Apps.
- **External visibility after approval:** publish one canonical directory link on ValuEdge's existing Connect page and add genuine, low-friction example prompts where relevant. No duplicate directory submissions under confusingly similar names.
- **Measure discovery and activation, separately:** keyword/search query -> directory listing view -> install -> OAuth connection when needed -> useful completed tool call -> first-week return -> paid conversion. Some events need ValuEdge-side instrumentation; avoid interpreting HTTP 200 or raw user-agent requests as successful human research sessions.
- **Baseline belongs to the connector, not the unpublished plugin:** the earlier Claude screenshot was a 30-day connector view (27 finished connections, 7 tool-using accounts, 60 calls, 20% tool error rate), not the new plugin's analytics. Capture an independent plugin baseline only after publication.
- **Evaluation cadence:** use seven full days for an initial observation period; compare meaningful search query cohorts at day 28. Change one listing variable per review cycle to reduce confounding, acknowledging the platform does not publish ranking weights.

### Evidence & exclusions

Official Anthropic docs identify manifest keywords as discovery tags and provide directory search-query / listing-view analytics after publication. They do **not** publish a reliable rule that adding more keyword variants alone moves a plugin up search rankings. The directory validator has informational warnings for directory-only fields on some Claude Code versions; preserve those fields for listings. Avoid fake installs/reviews, spam, mass near-duplicate plugins, unsupported security/financial claims, or guaranteed performance.
