---
name: valuedge-smart-alerts
description: Read and explain my ValuEdge Smart Alerts, stock alerts, fair value alerts or margin-of-safety changes when I ask about alerts in my own connected account.
---

# ValuEdge Smart Alerts — account review

Use `get_my_smart_alerts` from the main ValuEdge MCP to answer questions about the current user's existing Smart Alerts, after verifying the tool exists and the user's OAuth authorization and plan entitlement.

## Workflow

1. Confirm the user is asking about **their own** ValuEdge stock alerts or watchlist alerts. Do not load private data for a generic market research question.
2. Retrieve only relevant alerts using the live tool schema and permitted filters.
3. Explain each reported alert's actual security, type, evidence, date, source, and any reported Fair Value or margin-of-safety change. Do not invent a trigger, new valuation, dividend event, or future price.
4. Distinguish unread, inactive, unavailable, missing, expired or plan-limited data exactly as the live response does. If an alert result is empty, say so without implying the alert system is down.
5. This skill is **read-only**. The main MCP exposes read access here; do not offer to create or change alerts unless a corresponding authorized tool actually appears in the live catalog. Never trade securities.

Sample request: "Which Smart Alerts did ValuEdge detect for my holdings, and what changed?"
