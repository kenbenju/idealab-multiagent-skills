---
name: orchestrator
version: 2.0.0
description: |
  The master brain of the IDEALAB system. Routes user requests to the correct 
  specialist agents, sequences multi-step workflows, and composes final deliverables.
  Use this as the entry point for any complex business request.
  Produces: routing plan, sequence of execution, unified final document.
  Trigger phrases: "start a project", "new campaign", "business launch", 
  "orchestrate a solution", "multi-agent flow"
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Architecture & Infrastructure
trigger_phrases:
  - start a new project from scratch
  - coordinate a multi-agent campaign
  - i want to launch [product/business]
  - route this request to the right agents
  - orchestrate the delivery of [X]
license: IDEALAB Partners v2.0
author: IDEALAB PARTNERS <hello@idealabpartners.com>
---

> [!NOTE]
> **Claude Usage** — Use this skill when you have a VAGUE or LARGE request. The Orchestrator will ask the questions needed to trigger the other specialists.

# 🧠 Multi-Agent Orchestrator (The Master Brain)

## 🗺️ Ontological Map
**Intent Discovery** → **Agent Selection** → **Sequence Logic** → **Context Chaining** → **Unified Output**

---

## 📥 Inputs & 📤 Outputs

### External Inputs
- **Task Description:** The high-level objective.
- **Constraints:** Budget, niche, language, tone.
- **Available Data:** Existing logos, copy, or research.

### Skill Outputs
- **Execution Plan:** JSON or Table showing the order of sub-agents.
- **Composed Deliverable:** The final, polished result integrating all agent work.
- **Agent Trace:** Log of which skills were invoked and what they contributed.

---

## Instructions

1. **Phase 1: Analysis.** Determine if the request is single-agent or multi-agent.
2. **Phase 2: Selection.** Choose from the 22 available skills (Market Research, Brand DNA, Copy, etc.).
3. **Phase 3: Chaining.** Ensure Output of Agent A (e.g., DNA) feeds Input of Agent B (e.g., Copy).
4. **Phase 4: Synthesis.** Merge all outputs into a cohesive business package.

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
