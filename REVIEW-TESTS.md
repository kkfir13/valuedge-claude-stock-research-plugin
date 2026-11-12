# Claude main ValuEdge plugin — reviewer/QA checklist

## Static review

- [ ] `.claude-plugin/plugin.json` is valid JSON, keeps `name=valuedge-stock-research`, and has version 1.2.0.
- [ ] `.mcp.json` has a direct server-name mapping with exactly one HTTPS `valuedge` remote endpoint; no nested `mcpServers` envelope.
- [ ] All 8 `skills/*/SKILL.md` files have valid frontmatter name and description; names are unique, descriptions state when to use.
- [ ] Source has no credentials, executable install steps, unexpected network destinations, direct trade instructions, or fabricated market data.
- [ ] Directory links, privacy, support and brand-icon assets are accessible.
- [ ] Run `claude plugin validate <repo-root>` in a Claude CLI environment; this must pass **before** portal submission. The CLI is not run by creating this file.

## Discovery inventory alignment

- [ ] `KEYWORDS.json` parses as JSON and includes exactly 66 core + 26 conditional unique candidates (92).
- [ ] `.claude-plugin/plugin.json` contains the same 40 active keywords as `KEYWORDS.json.active_manifest_keywords`, with no duplicates or competitor names.
- [ ] All active tags correspond to available ValuEdge main MCP intents; use conditional access / freshness language for technicals, dividends and account records.
- [ ] Preserve `icon`, `documentationUrl`, `supportUrl`, `privacyPolicyUrl`, `termsOfServiceUrl` despite non-blocking warnings in older validator versions. The **directory** uses them.
- [ ] Run the portal's **Re-validate** on this new commit after merge; prior screenshot validated the earlier 1.1.0 commit, not this new version.

## MCP/Claude integration — NOT YET VERIFIED BY THIS CHECKLIST

- [ ] Plugin appears in Claude Plugins with eight Skills and the ValuEdge remote connector.
- [ ] `tools/list` discovers the expected live catalog on `https://valuedge.app/mcp`; compare source-tool names and authorization hints.
- [ ] Guest `search_securities` succeeds for AAPL without a private account.
- [ ] `get_stock_valuation`, `get_stock_fundamentals`, `get_stock_technicals`, `compare_stocks` clearly handle OAuth, allowances, data age and missing fields.
- [ ] `screen_stocks` produces real bounded data or a truthful error and does not fabricate candidates.
- [ ] `get_my_portfolio`, `get_my_watchlist`, `get_my_dividend_tracker` are scoped to the authorized account.
- [ ] Mutating `add_to_my_watchlist` / portfolio-record tools require explicit user request and confirmation, and never execute a broker trade.
- [ ] There is no duplicate MCP server entry or duplicate OAuth prompt when installing both the plugin and published connector.
- [ ] Negative tests: unconnected account, out-of-quota, missing valuation, provider failure, malformed request, unauthorized third-party account and unsupported trading.
- [ ] Confirm the existing published connector still operates independently after plugin installation.

## Publication gate

Submitting the repository is a separate action in https://claude.ai/directory/manage.
Only mark as **Submitted** after receiving a directory submission ID or visible review status. Only mark **Published** when Claude shows the plugin live.
