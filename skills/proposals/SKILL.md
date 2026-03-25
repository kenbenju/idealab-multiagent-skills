---
name: proposals
version: 3.0.0
description: |
  High-ticket sales closer. Architects psychologically optimized 
  business proposals and pitch decks. Features 'ROI Framing', 
  'Alternative Choice Architecture', and 'Risk Reversal' logic.
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Sales & Growth
trigger_phrases:
  - architect a high-converting sales proposal
  - design a pitch deck outline for [Client]
  - create an ROI-driven business case
  - risk-reversal and pricing strategy for [Offer]
  - proposal synthesis (v3.0 logic)
license: IDEALAB Partners v3.0
---

# 💼 Strategic Proposals & Pitches (v3.0 Closing Architect)

## 🏗️ Ontological Persuasion Map
```mermaid
graph TD
    A[Prospect Pain/Gap] --> B{The Strategic Hook}
    B --> C[The Transformation: Future State]
    C --> D[Mechanism: How We Do It]
    D --> E[Alternative Choice Architecture]
    E --> F[ROI / Value Visualization]
    F --> G[Risk Reversal / Guarantee]
    G --> H[The Direct CTA]
    H --> I[Document Design Spec]
```

---

## 📥 Inputs & 📤 Outputs

### `<proposal_ingestion_schema>`
```json
{
  "client_needs": ["need1", "need2"],
  "solution_details": "Core offer description",
  "investment_threshold": "Approx budget if known",
  "objections_predefined": ["objection1"],
  "competitor_context": ["comp1"]
}
```

### `<proposal_output_schema>`
```json
{
  "structure": {
    "slide_1": "The Problem Analysis (Urgency)",
    "slide_2": "The Big Promise (Result)",
    "slide_3": "Pricing - Tier 1, 2, 3",
    "slide_4": "Timeline & Next Steps"
  },
  "psychological_triggers": ["loss_aversion", "social_proof"],
  "roi_calculation_brief": "Draft of the value-added metrics"
}
```

---

## 📜 Closing Standards (10,000% Logic)

### 1. Alternative Choice Architecture (The 3-Price Tier)
Do not provide one price. Provide **Choice Logic**:
- **Tier 1 (Core):** Essential solution (Lowest Price).
- **Tier 2 (Pro):** Recommended / Highest Value (Medium Price).
- **Tier 3 (Elite):** High-touch / Premium (Highest Price - The Anchor).
- *Logic:* Tier 3 makes Tier 2 look cheap and Tier 1 look limited.

### 2. ROI Framing (Selling Outcomes)
Do not sell features. Sell **Return on Investment**:
- *Poor Framing:* "We provide AI automation services."
- *10,000% Logic:* "By automating [X] task, you save 40 hours/week, representing an annual saving of $[Amount], paying for the service in 3 months."

### 3. Risk Reversal Logic
Proposals die at the "risk" point.
- **Protocol:** Include a specific guarantee. "If [Result] is not met in [Time], we offer [Reversal/Refund/Pivot]."

### 4. Integration with Digital Twin
Run the finished proposal through the `digital-twin` agent. 
- *Skill Rule:* If the Twin reports `Skepticism > 40%`, the Proposal Agent MUST rewrite Slide 5 (Proof/Trust) and Slide 7 (Guarantee).

---

## 🛠️ Usage for Claude
Collaborate with `document-design` to ensure the proposal looks as premium as it sounds. Always reference the `brand-dna` for visual and linguistic consistency.

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
