# ValuEdge Stock Research for Claude

This plugin pairs three focused research skills with ValuEdge's existing remote MCP connector. It supports public-company screening, valuation and fundamentals review, and read-only analysis of the installing user's authorized ValuEdge portfolio. It does not place trades, change holdings, or promise investment outcomes.

## Connect

The plugin declares ValuEdge's remote MCP endpoint at `https://valuedge.app/mcp`. On Claude, add or connect the ValuEdge connector from the plugin's Connectors tab and complete ValuEdge's own authorization when prompted. Public-company research tools can be used without ValuEdge sign-in. Portfolio, watchlist, and Smart Alerts tools require the user's own OAuth authorization and an eligible ValuEdge Trial or Unlimited account. This plugin contains no API keys, passwords, tokens, or user data.

## Workflows

- **Portfolio review:** summarize holdings and portfolio-level exposure using the user-authorized read-only account tools.
- **Stock screening:** run bounded screens from supported NYSE and NASDAQ securities. ValuEdge documents a candidate window of up to 60 and a maximum of 12 returned results; the skill preserves those limits and the live tool schema.
- **Valuation and comparison:** review ValuEdge valuation and fundamentals results, resolve ambiguous securities first, and compare between two and six tickers where supported.

The skills identify returned figures as ValuEdge data, preserve dates and limitations, and treat missing data as unavailable rather than zero. They do not tell users to buy, sell, or trade securities.

## Data handling

The plugin sends requests only to the declared ValuEdge MCP connector. Requests may contain security identifiers, ticker symbols, screening criteria, or market queries needed to answer the user. ValuEdge's Privacy Policy explains that these requests may be processed by its market-data provider, FMP, and describes account-data and operational-log retention, including logs generally kept for up to 90 days. Private portfolio data is available only after the user authorizes their own account. See [ValuEdge Privacy Policy](https://valuedge.app/privacy) and [Terms of Service](https://valuedge.app/terms).

## License and brand

MIT applies to the original plugin instructions and documentation in this repository. It does not grant rights to ValuEdge names or marks, product services, or third-party market data. The bundled ValuEdge logo is a brand asset and is not included in the MIT grant.
