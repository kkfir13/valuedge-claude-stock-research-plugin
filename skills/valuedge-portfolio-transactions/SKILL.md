---
name: valuedge-portfolio-transactions
description: Record, edit or remove a transaction or holding in my own ValuEdge portfolio tracker when I explicitly request a portfolio-record correction, not a broker trade.
---

# Manage portfolio records in ValuEdge

Only handle explicit user-authorized portfolio **record** management, not order placement or account transfers. The main MCP may expose `list_my_portfolio_transactions`, `record_my_portfolio_transaction`, `edit_my_portfolio_transaction`, `remove_my_portfolio_transaction` and `remove_my_portfolio_holding`. Inspect live schemas and account-scoped permissions before acting.

## Method

1. Confirm the target account/portfolio, security, date, quantity, price, currency, transaction type and record identifiers required by the actual tool schema. Never infer or invent missing facts.
2. Read existing records with the minimal tool calls needed to avoid duplicates or incorrect edits.
3. Show the exact intended mutation in plain language and obtain the user's explicit confirmation **before** writes; for removals, explain what will be removed and whether it can be undone, when known.
4. Apply only the requested change, obeying OAuth authorization, plan limits, tool hints and error responses. Never use this to access another user's account.
5. Verify the returned result, then report precisely what changed. If the write is rejected or uncertain, do not claim success or issue an unrequested retry.

No broker orders, securities transfers, trade execution or auto-rebalancing are offered by this skill.
