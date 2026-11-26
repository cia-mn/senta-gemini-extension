# Senta for Gemini CLI

Official [Gemini CLI](https://geminicli.com/) extension connecting Gemini to **Senta (ХАБЭА / HSE)** via Senta's unified remote MCP gateway (`https://control.senta.mn/mcp`).

Query work permits, safety observations, inspections, instructions, projects, and org reference codes — or create safe non-signing drafts — using your existing Senta account.

---

## Install

```bash
gemini extensions install https://github.com/cia-mn/senta-gemini-extension
```

When prompted by Gemini CLI, complete the Senta OAuth 2.1 SMS sign-in in your browser.

---

## Manage Your Organization Scope & Access Level

You control which organizations Gemini can access and whether each organization is **Off**, **Read-only**, or **Read + Draft/Write** at any time from **Миний Senta**:

- Open **[https://app.v2.senta.mn/account](https://app.v2.senta.mn/account)** → **AI / MCP хандалт**
- Toggle each organization between:
  - **Хаалттай (`off`)** — blocked immediately
  - **Зөвхөн унших (`read`)** — default; 14 read-only tools
  - **Унших + Ноорог (`write`)** — adds 3 safe non-signing tools
- Revoke connected AI assistants anytime from **Холбогдсон AI апп ба төхөөрөмжүүд**.

---

## Available Tools

### Organization-Free HSE & Training Standards (Works Even Without an Organization!)
| Tool | Description |
| :--- | :--- |
| `list_hse_standards` | List all Mongolian HSE laws, training standards (`MNS 4969:2000`, `ХАБЭА-н сургалтын журам`), official document formatting (`MNS 5140:2026`), and HSE document practice guides |
| `search_hse_knowledge` | Keyword search across all Mongolian HSE standards, training rules, PPE, risk assessment, and document templates |
| `get_hse_document_guide` | Read the full text of any standard or document guide by slug to draft standards-compliant documents |

### Discovery & Read-Only Organization Tools (enabled by default)
| Tool | Description |
| :--- | :--- |
| `list_organizations` | List your Senta organizations, roles, and MCP access levels (`off`/`read`/`write`) |
| `list_permits`, `get_permit`, `permit_metrics` | Search, inspect, and count work permits |
| `list_safety_observations`, `get_safety_observation`, `safety_observation_stats` | Search, inspect discussions, and aggregate safety observations |
| `list_inspections`, `get_inspection` | List and read inspection checklists & answers |
| `list_instructions`, `get_instruction` | List and read safety instructions (зааварчилгаа) |
| `list_projects`, `list_reference_codes`, `list_users`, `list_work_types` | Look up projects, PPE/hazard codes, people, and trades |

### Safe Non-Signing Write Tools (only when `write` is enabled for the org)
| Tool | Description |
| :--- | :--- |
| `create_safety_observation` | Report a new safety hazard observation |
| `add_observation_comment` | Post a comment on an existing safety observation |
| `create_instruction_draft` | Create an **unpublished** (`publish: false`) instruction draft for review in Senta Console |

> **Compliance & Privacy (MNS 4969:2000):** Phone numbers and national register/passport numbers are masked automatically before leaving Senta. Legal signatures (briefings, permits, waivers), approvals, and destructive deletes are never exposed via MCP.

---

## Support & Privacy

- Website: [https://senta.mn](https://senta.mn)
- Account & MCP Portal: [https://app.v2.senta.mn/account](https://app.v2.senta.mn/account)
- Contact: `info@cia.mn`
