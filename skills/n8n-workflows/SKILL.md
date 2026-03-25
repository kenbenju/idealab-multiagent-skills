---
name: n8n-workflows
version: 2.0.0
description: |
  Specialized skill for designing, building, and documenting complex automation 
  workflows using n8n. Integrates Claude agents with external APIs, databases, 
  and business tools.
  Produces: n8n JSON workflow schemas, node transformation logic, error handling 
  strategies, and trigger-action maps.
  Trigger phrases: "build n8n workflow", "automate this in n8n", "n8n node setup",
  "connect agents to zapier/n8n", "automation pipeline"
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Automation & Integration
trigger_phrases:
  - design a workflow for n8n
  - generate n8n json
  - connect my agent to n8n
  - automate lead capture in n8n
  - n8n error handling logic
license: IDEALAB Partners v2.0
author: IDEALAB PARTNERS <hello@idealabpartners.com>
---

# 🤖 n8n Automation & Workflow Engineering

## 🗺️ Ontological Map (Logic Flow)
**Input** (Requirements) → **Logic** (Node Mapping & Transformation) → **Integration** (API/Auth) → **Output** (n8n JSON)

---

## 📥 Inputs & 📤 Outputs

### External Inputs
- **Process Map:** Description of the manual workflow to automate.
- **Tools List:** Apps involve (e.g., Slack, Gmail, Airtable, CRM).
- **Trigger Type:** Webhook, Schedule, or App-based.

### Skill Outputs
- **Workflow JSON:** Ready-to-import n8n schema.
- **Node Configurations:** Specific settings for complex nodes (HTTP Request, Code, Merge).
- **Data Transformation:** JavaScript code for 'Code' nodes to clean input.

---

## Step-by-Step Instructions

### Step 1 — Define the Blueprint
Identify the **Trigger**, **Actions**, and **Filters**.
- Trigger: *When a new lead enters CRM...*
- Filter: *If lead quality > 7...*
- Action: *Notify Slack and Send Welcome Email.*

### Step 2 — Data Mapping & Ontology
Map how data flows between nodes. Ensure "ID" consistency across disparate tools.

### Step 3 — Error Handling (The "Safety" Loop)
Always add an Error Trigger or use "Continue on Fail" logic for non-critical nodes.

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
