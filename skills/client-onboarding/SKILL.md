---
name: client-onboarding
version: 3.0.0
description: |
  Operational success architect. Designs the transition from 
  'Prospect' to 'Active Partner'. Builds kickoff agendas, 
  data collection forms, and 'First 30 Days' success roadmaps.
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Sales & Growth
trigger_phrases:
  - design a client onboarding workflow for [Service]
  - create a kickoff meeting agenda and success roadmap
  - build a data-gathering intake form for [Project]
  - 30-day success plan for [Client Name]
  - client success architecture (v3.0)
license: IDEALAB Partners v3.0
---

# 🤝 Client Onboarding & Success (v3.0 Operations Architect)

## 🗺️ Ontological Success Map
```mermaid
graph TD
    A[Signed Contract] --> B{Kickoff Trigger}
    B --> C[Intake Form (Data Collection)]
    C --> D[Success Vision: The North Star]
    B & D --> E[Internal Team Briefing]
    E --> F[Client Kickoff Meeting]
    F --> G[Action: The First 30 Days]
    G --> H[Milestone 1: The First Win]
    H --> I[Transition to Delivery Agents]
```

---

## 📥 Inputs & 📤 Outputs

### `<onboarding_request>`
- **Client Vertical:** Industry context.
- **Expected Outcome:** Primary transformation goal.
- **Team Roles:** Who is the Account Manager? Who is the Tech Lead?
- **Urgency:** Preferred kickoff date.

### `<onboarding_output_schema>`
```json
{
  "welcome_package": {
    "checklist": ["Item 1", "Item 2"],
    "intake_link": "URL to form/doc",
    "timeline": "Week 1 to Week 4 breakdown"
  },
  "kickoff_agenda": ["Point 1: Intro", "Point 2: Vision Align"],
  "first_30_days_goal": "One measurable win"
}
```

---

## 📜 Success Standards (10,000% Logic)

### 1. The 'North Star' Metric
Identify the ONE outcome that the client equates to success.
- **Protocol:** "By the end of day 30, we will have [Measurable Result X] live."

### 2. Intake Friction Reduction
Do not ask for 100 things at once. 
- **Skill Logic:** Use a "Tiered Intake". 
- *Tier 1 (Immediate):* Access to accounts.
- *Tier 2 (Wait):* Deep strategy interviews.

### 3. Internal Alignment Briefing
Generate a brief for the `multi-agent` swarm. 
- *Action:* Summarize the client's "Taboo Words" (from `anti-bias`) and "Competitor Gaps" (from `market-research`) so the delivery agents don't have to re-research.

### 4. ROI Re-Confirmation
The onboarding agent must restate the ROI mentioned in the `proposals` agent to ensure expectations are synchronized.

---

## 🛠️ Usage for Claude
When a user says "I just closed a deal," the Orchestrator should trigger this skill and `memory` to pull all sales data into the success roadmap.

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
