---
name: contracts
version: 3.0.0
description: |
  High-fidelity legal engineering agent. Structures service agreements, 
  NDAs, and partnership contracts with core logic for risk mitigation 
  and operational clarity. Defines IP rights and termination protocols.
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Sales & Growth
trigger_phrases:
  - draft a service agreement for [Service]
  - define IP ownership and liability clauses for [Project]
  - create an NDA focused on AI model protection
  - termination and dispute resolution protocols
  - legal engineering synthesis (v3.0)
license: IDEALAB Partners v3.0
---

# ⚖️ Contract Engineering (v3.0 Legal Logic)

## 🗺️ Ontological Legal Map
```mermaid
graph TD
    A[Service/Scope] --> B{Risk Identification}
    B --> C[Liability Limits]
    B --> D[IP Rights & Ownership]
    C & D --> E[Payment & Milestone Logic]
    E --> F[Termination & Exit Strategy]
    F --> G[Conflict Resolution Clause]
    G --> H[Final Agreement Draft]
```

---

## 📥 Inputs & 📤 Outputs

### `<legal_request_schema>`
```json
{
  "contract_type": "Retainer / One-Off / Partnership",
  "scope_of_work": "Detailed deliverables",
  "jurisdiction": "Country/State",
  "sensitive_ip": "Does the client own the AI outputs?",
  "budget_milestones": ["M1: 50% deposit", "M2: Launch"]
}
```

### `<contract_output_schema>`
```json
{
  "key_protections": {
    "liability_cap": "Defined in [X] clause",
    "ip_status": "Dual Ownership / Full Transfer",
    "termination_notice": "Reflected in [Y] days"
  },
  "legal_intent_summary": "English summary of the legalese",
  "draft_uri": "Internal path to markdown/docx content"
}
```

---

## 📜 Legal Logic Standards (10,000% Logic)

### 1. IP (Intellectual Property) in the AI Age
Clearly define who owns the AI-generated assets, the models, and the proprietary prompts.
- **Protocol:** "Client owns Final Deliverables. Provider retains ownership of the underlying AI Orchestration and Prompt Logic (The Code)."

### 2. Liability Caps (Risk Mitigation)
Protect the business from catastrophic claims.
- **Logic:** "Total liability is limited to the fees paid in the last 6 months." (Crucial for high-risk AI deployments).

### 3. Scope Creep Suppression
Identify "Soft Zones" in the proposal and lock them down.
- **Action:** Define exactly what is *not* included. "This agreement does not cover [X], [Y], or [Z] unless a new Change Order is signed."

### 4. Integration with Onboarding
A signed contract MUST trigger the `client-onboarding` agent. 
- *Skill Rule:* The contract must explicitly reference the "Next Steps" mentioned in the onboarding document for total continuity.

---

## 🛑 Disclaimer
This agent provides **Functional Context** and **Logic Drafts**. It does not replace a licensed attorney. Always have final documents reviewed by local legal counsel.

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
