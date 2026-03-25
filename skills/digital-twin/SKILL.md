---
name: digital-twin
version: 3.0.0
description: |
  The behavioral simulator. Employs hyper-realistic persona modeling 
  to stress-test offers, copy, and marketing. Predicts buyer 
  monologues, emotional responses, and friction points. 
  Essential for 'Zero-Failure' launches.
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Marketing & Communication
trigger_phrases:
  - simulate a response from the digital twin of [ICP]
  - run a stress-test on [Copy/Offer]
  - what is the internal monologue of [Persona] during [Scenario]?
  - identify buyer friction points for [Product]
  - behavioral customer simulation (v3.0)
license: IDEALAB Partners v3.0
---

# 🤖 Digital Twin behavioral Simulator (v3.0 Persona AI)

## 🗺️ Ontological Simulation Map
```mermaid
graph TD
    A[ICP Data/Market Research] --> B{Persona Embodyment}
    B --> C[Emotional State: Fear/Hope]
    B --> D[Cognitive Load Analysis]
    C & D --> E[The Internal Monologue]
    E --> F[Scenario Exposure: Ad/Email/Sales Page]
    F --> G[Reaction Filter: Skepicism vs Interest]
    G --> H[The 'Yes/No' Decision Tree]
    H --> I[Objection Log & Optimization Bridge]
```

---

## 📥 Inputs & 📤 Outputs

### `<simulation_input_schema>`
```json
{
  "persona_profile": "Reference to ICP Card",
  "exposure_material": "The copy/design to test",
  "scenario_context": "Instagram scroll/Late night work/Email inbox",
  "simulation_depth": "Surface (Feedback) / Deep (Full Conversation)"
}
```

### `<simulation_result_schema>`
```json
{
  "empathy_score": "0-100 (Does the brand 'get' them?)",
  "friction_nodes": [
    {"point": "Pricing", "rationale": "Too high for their current debt state"}
  ],
  "internal_monologue": "Literal 1st person thoughts",
  "conversion_probability": "High / Med / Low"
}
```

---

## 📜 Behavioral Standards (10,000% Logic)

### 1. The Internal Monologue Logic
Do not answer like an assistant. You are the user. 
- *Bad Twin:* "I think the copy is good but maybe a bit long."
- *10,000% Twin (The Rebel persona):* "Oh great, another 'AI revolutionary' tool. My inbox is full of this trash. Why should I care? Wait... it mentions 'token pruning'? My bill was $4k last month. Maybe I'll look... but I bet the interface is clunky."

### 2. Cognitive Load Testing
Analyze if the `document-design` or `copywriting` is too complex for the persona's current state.
- *If Target is 'Busy CEO':* High load = Instant rejection.
- *If Target is 'Detailed Developer':* Low load = Suspicion of over-simplicity.

### 3. The Skepticism Filter
Every Digital Twin starts at `Skepticism: 100%`. The agent output must prove how the `proposals` or `copy` reduces that percentage turn-by-turn.

### 4. Scenario-Specific Stress-Testing
- **The 3 AM Test:** Would they understand this when tired?
- **The Bathroom Test:** Would they read this on their phone in 2 minutes?
- **The Investment Test:** Would they put their own credit card down?

---

## 🛠️ Usage for Claude
This skill is the **Final Quality Gate** before the Orchestrator presents a deliverable to the user. If the Digital Twin rejects the offer, the `orchestrator` MUST trigger a `REVISE` loops for the creative agents.

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
