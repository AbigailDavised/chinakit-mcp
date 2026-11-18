---
name: chinakit
description: "Evaluate China work permit Category A/B/C points, border medication legality, expatriate IIT fringe tax optimization, visa-free/TWOV routing, Hague Apostille rules, and CAAC powerbank limits via ChinaKit's stateless MCP server."
homepage: https://chinakit.io
version: 1.0.0
license: MIT
compatibility: "Works with Hermes Agent, Claude Code, Cursor, Windsurf, and any MCP client supporting Streamable HTTP."
metadata:
  homepage: "https://chinakit.io"
  mcp_endpoint: "https://chinakit.io/api/mcp"
  version: "1.0.0"
  hermes:
    category: travel
    tags: [china-travel, visa-free-transit, work-permit, customs-meds, expat-tax]
---

# ChinaKit — Stateless China Compliance & Travel MCP Skill

Connect any MCP-compatible AI agent to ChinaKit's public read-only Streamable HTTP server at `https://chinakit.io/api/mcp`. Zero sign-in or API keys required.

## Endpoint Configuration

```json
{
  "mcpServers": {
    "chinakit": {
      "type": "streamable-http",
      "url": "https://chinakit.io/api/mcp"
    }
  }
}
```

## Direct JSON-RPC 2.0 Verification

```bash
curl -s -X POST https://chinakit.io/api/mcp \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"check_china_customs_medication_legality","arguments":{"medicationQuery":"Adderall"}}}'
```

## Tools Inventory (8 Read-Only Tools)

- `calculate_china_work_permit_points`: SAFIEA Category A/B/C rubric & 6x salary exemption calculator.
- `check_china_customs_medication_legality`: Controlled psychotropic/narcotic border limits & Red Channel checklist.
- `calculate_china_expat_iit_and_bonus`: Expatriate Individual Income Tax & Seven Fringe Exemptions optimizer.
- `validate_china_transit_and_visa_free_entry`: 15/30d visa-free & A-B-C TWOV itinerary validator.
- `query_china_document_apostille_steps`: Hague Apostille vs Consular legalization rules & federal trap checks.
- `recommend_china_essential_apps_and_payment`: Passport KYC setup playbooks for Alipay, WeChat Pay, 12306 & Didi.
- `lookup_china_destination_foreigner_guide`: 331 verified attraction passport scan & card readiness records.
- `calculate_caac_powerbank_and_alipay_split`: CAAC 100Wh/160Wh watt-hour gate & ¥200 Alipay fee splitter.
