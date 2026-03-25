---
name: n8n-workflows
version: 3.0.0
description: |
  Enterprise logic bridge for n8n.ai and external API automation. 
  Designs JSON structures for HTTP Request nodes, error handling 
  with 'Wait' nodes, and complex conditional flows. 
  Ensures Claude-to-Automation parity.
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Architecture & Infrastructure
trigger_phrases:
  - design a n8n workflow for [Automated Task]
  - create JSON mapping for an n8n node
  - build a webhook-to-database logic for [X]
  - error recovery protocol for [API]
  - n8n node-tier architecture
license: IDEALAB Partners v3.0
---

# 🕸️ n8n Enterprise Workflow Bridge (v3.0 Automation Architect)

## 🗺️ Ontological Automation Map
```mermaid
graph TD
    A[Trigger: Webhook/Schedule] --> B{Data Ingestion}
    B --> C[AI Agent/LLM Node]
    C --> D{Conditional Logic}
    D -->|True| E[Action: CRM/DB/Email]
    D -->|False| F[Wait/Correction Loop]
    E --> G[Feedback Loop back to A]
```

---

## 📥 Inputs & 📤 Outputs

### `<workflow_spec_schema>`
```json
{
  "automations_objective": "e.g., Cold Email Inbound Processing",
  "integration_points": ["Google Sheets", "Salesforce", "WhatsApp"],
  "security_tier": "API Key / OAuth2 / Local Tunnel",
  "performance_kpi": "Execution time < 5s"
}
```

### `<node_configuration_schema>`
```json
{
  "node_type": "n8n-nodes-base.httpRequest",
  "parameters": {
    "method": "POST",
    "url": "https://api.example.com/v1/",
    "authentication": "headerAuth",
    "bodyParameters": {
      "data": "={{ $json.content }}"
    }
  },
  "error_logic": "Retry on 429 after 30s"
}
```

---

## 📜 Automation Integrity Protocols

### 1. The "Wait Node" Strategy
Claude must design workflows that handle AI latency.
- **Protocol:** If the LLM node takes >10s (e.g., deep reasoning), use an asynchronous `Webhook Response` to acknowledge receipt before finishing the logic.

### 2. JSON Payload Mapping
Ensure data types match the destination.
- *Issue:* Sending a "String" to a "Date" field in CRM.
- *Skill Logic:* Use a `Map` node instruction to force format casting: `{{ new Date($json["created_at"]).toISOString() }}`.

### 3. Loop Protection
Prevent runaway credits.
- **Constraint:** All recursive loops must have a `max_iterations: 5` counter.

### 4. Claude-to-n8n Schema Parity
Ensure the Output of `copywriting` is mapped perfectly to an `Email` node.
1. Define the `Subject`, `Body`, and `Variables` in a JSON block.
2. Instruct the user to copy-paste this block into the n8n `Expression` field.

---

## 🛠️ Usage Hint
This skill is the "Hands" of the ecosystem. While other agents "Think", `n8n-workflows` implements the "Action".

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
