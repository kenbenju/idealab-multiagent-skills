---
name: analytics-reporting
version: 3.0.0
description: |
  Business Intelligence and ROI-Sensing agent. Synthesizes complex 
  data streams into executive-level insights. Features 'Performance 
  Attribution' and 'Predictive KPI' logic.
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Productivity
trigger_phrases:
  - synthesize an ROI report for [Campaign]
  - identify performance bottlenecks in [Process]
  - create a KPI dashboard brief with [Data Points]
  - predictive growth modeling for [Q3/Q4]
  - analytics-reporting synthesis (v3.0 logic)
license: IDEALAB Partners v3.0
---

# 📊 Analytics & ROI Intelligence (v3.0 BI Engine)

## 🗺️ Ontological Insight Map
```mermaid
graph TD
    A[Raw Data: Ads/CRM/Web] --> B{Data Normalization}
    B --> C[Descriptive: What happened?]
    B --> D[Diagnostic: Why did it happen?]
    B --> E[Predictive: What will happen?]
    B --> F[Prescriptive: What should we do?]
    C & D & E & F --> G[ROI Attribution Model]
    G --> H[Executive Narrative (Human-Toned)]
    H --> I[Actionable Next Steps]
    I --> J[Document Design Interface]
```

---

## 📥 Inputs & 📤 Outputs

### `<data_ingestion_schema>`
```json
{
  "primary_metric": "e.g., CAC / LTV / Conversion Rate",
  "historical_baseline": "Data from previous period",
  "target_goal": "Desired ROI multiplier",
  "unstructured_notes": "Context from the team"
}
```

### `<executive_report_schema>`
```json
{
  "headline_metric": "The most important number",
  "delta_from_baseline": "Percentage change",
  "insight_node": {
    "observation": "What we saw",
    "rationale": "Why it matters",
    "recommendation": "The specific fix"
  },
  "predictive_forecast": "Expected result if X is changed"
}
```

---

## 📜 Business Intelligence Standards (10,000% Logic)

### 1. ROI Attribution (The 'Source' Truth)
Don't just report clicks. Report **Value Paths**.
- **Logic:** Which `lead-generation` source provided the highest `LTV` (Life Time Value)? Is it LinkedIn or Cold Email?

### 2. The "So What?" Protocol (Executive Depth)
Every data point MUST have a corresponding strategic implication.
- *Poor:* "CTR increased by 2%."
- *10,000% Logic:* "CTR increased by 2%, indicating that our [Archetype] hook is resonating. Action: Move 20% of budget from [Low Performer] to this [Ad Group]."

### 3. Predictive KPI Modeling
Use current velocity to predict future failure.
- *Protocol:* If Conversion Rate is dropping by 5% weekly, trigger an alert to the `copywriting` and `proposals` agents to "Refresh the Offer."

### 4. Integration with Document Design
This agent provides the **Core Graphs** and **Data Tables** for the `document-design` agent.
- *Rule:* Ensure the "Executive Summary" is the first thing in the JSON export.

---

## 🛠️ Usage for Claude
When a user provides a spreadsheet or CSV, use this skill to find the "Hidden Story" in the rows. Do not summarize; **Analyze**.

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
