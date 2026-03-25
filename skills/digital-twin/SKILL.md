---
name: Digital Twin Agent
version: 1.0.0
description: Simulates a detailed behavioral model of a target customer persona — capable of responding to scenarios, predicting reactions, stress-testing messaging, and generating insights about buyer psychology.
author: IDEALAB PARTNERS <hello@idealabpartners.com>
license: IDEALAB Partners v1.0
inputs:
  - name: persona_source
    type: object
    description: ICP card, real customer data, or interview transcripts to base the twin on
    required: true
  - name: twin_name
    type: string
    description: Name for this persona twin (for reference)
    required: false
  - name: scenario
    type: string
    description: Specific scenario to simulate (e.g. "receives cold email", "sees Instagram ad", "visits landing page")
    required: false
  - name: stress_test_inputs
    type: array
    description: Messages, offers, or copy to test against the persona's reactions
    required: false
outputs:
  - name: persona_profile
    type: object
    description: Detailed behavioral persona card (psychology, daily routine, decision filters, objections)
  - name: behavior_map
    type: object
    description: Decision-making journey map from awareness to purchase
  - name: scenario_simulation
    type: object
    description: Twin's simulated reaction to provided scenario (thoughts, emotions, actions)
  - name: stress_test_results
    type: array
    description: Evaluation of each test input from the twin's perspective (resonates / doesn't / why)
  - name: insights
    type: array
    description: Actionable insights about how to better communicate with this type of buyer
agents_required:
  - market-research
  - crm
tags:
  - persona
  - simulation
  - behavioral-modeling
  - audience
  - psychology
---

# 🤖 Digital Twin Agent — Persona Simulation & Behavioral Modeling

## Objective

Create a living, simulatable model of your ideal customer that thinks, reacts, and makes decisions like a real person — so you can test your marketing, offers, and messages before spending a single dollar.

---

## Trigger

Activate when you need to: understand your audience deeply, stress-test copy or an offer, map the buyer journey, or simulate how a specific person type would react to your brand.

---

## Step-by-Step Instructions

### Step 1 — Build the Persona Profile

```
## Digital Twin Profile — [Twin Name]

### Identity
- Name: [Fictional but realistic]
- Age:
- Location:
- Occupation / Role:
- Income bracket:
- Family status:

### A Day in Their Life (6am–10pm narrative)
[Write a 150-word narrative of their typical day — what they see, do, feel, and scroll through]

### Psychology Stack
- Core desire (what they really want):
- Dominant fear (what keeps them up at night):
- Worldview (how they see the market / your category):
- Self-image (how they see themselves vs. how they want to be seen):
- Identity statement ("I am the kind of person who..."):

### Decision-Making Filters
When evaluating a new solution, they ask (in order):
1. "Is this for someone like me?" → [Tribal fit check]
2. "Can I trust this?" → [Credibility check]
3. "Will this actually work for me?" → [Relevance check]
4. "Can I afford this?" → [Price rationalization]
5. "Is now the right time?" → [Urgency check]

### Top 5 Objections (in their voice)
1. "But what if..."
2. "I've already tried..."
3. "I don't have time for..."
4. "What makes you different from..."
5. "I need to think about..."
```

### Step 2 — Map the Buyer Journey

```
AWARENESS STAGE
- Where they are: [Platform, community, content type]
- What triggered awareness: [Event, pain flare, social scroll]
- How they feel: [Curious but skeptical]
- What they do next: [Follow, save, search]

CONSIDERATION STAGE
- Research behavior: [Reviews, Google, ask friends, watch YouTube]
- Comparison criteria: [Price, proof, personality, process]
- Decision influencers: [Who do they trust in this space?]

DECISION STAGE
- Final trigger to buy: [Deadline, bonus, testimonial, personal outreach]
- Biggest hesitation at checkout: [Price, fear of failure, partner approval]
- Post-purchase emotion: [Relief, excitement, hope, mild regret]

LOYALTY STAGE
- What makes them stay: [Results, community, ongoing value]
- What makes them refer: [Pride, incentive, genuine transformation]
```

### Step 3 — Run Scenario Simulation

For each provided `scenario`, simulate the twin's:

1. **First Thought** (immediate gut reaction in 1 sentence)
2. **Emotional Response** (excited / skeptical / confused / triggered — and why)
3. **Mental Questions** (what they're thinking but not saying)
4. **Likely Action** (click, ignore, save, DM, buy, unfollow)
5. **What Would Change Their Mind** (if their initial action is not ideal)

### Step 4 — Stress-Test Inputs

For each message, headline, or offer in `stress_test_inputs`, rate:

| Input | Resonance (1-10) | Friction Point | What Works | What Doesn't | Suggested Fix |
|-------|-----------------|---------------|-----------|--------------|---------------|
| "Headline A" | 7 | Price framing | Hook is strong | CTA too vague | "Change 'Learn more' to 'See the method'" |

### Step 5 — Generate Strategic Insights

From all the above, extract 5–7 actionable insights:
- **Insight**: [Observation about this persona type]
- **Implication for marketing**: [What to change or emphasize]
- **Implication for product**: [What feature/benefit to highlight or add]

---

## Output Format

```json
{
  "persona_profile": {
    "name": "Sofía, 34, Coach de Bienestar",
    "core_desire": "Ser reconocida como experta sin sonar vendedora",
    "dominant_fear": "Invertir y no ver resultados",
    "decision_filters": ["¿Es para alguien como yo?", "¿Funciona?"]
  },
  "behavior_map": {
    "awareness": "Ve Reel de Instagram → guarda → sigue",
    "consideration": "Busca reseñas → revisa perfil → lee bio",
    "decision": "Recibe DM personalizado → compra en 48h"
  },
  "scenario_simulation": {
    "scenario": "Receives cold email",
    "first_thought": "Otro más vendiendo lo mismo...",
    "emotional_response": "skeptical",
    "likely_action": "Ignora si primer párrafo no es específico",
    "what_changes_mind": "Mencionar su industria específica en el asunto"
  },
  "insights": [
    {
      "insight": "Esta persona compra con el corazón y justifica con la razón",
      "implication_marketing": "Liderar con historia emocional, cerrar con datos",
      "implication_product": "Incluir comunidad como beneficio central"
    }
  ]
}
```

---

## Integration Points

- **Receives from**: `market-research` (ICP), `crm` (real customer interaction data)
- **Sends to**: `copywriting` (persona language and objections), `social-media-design` (persona content preferences), `brand-dna` (audience insights)

---

*© 2026 IDEALAB PARTNERS — Licensed under IDEALAB Partners v1.0*
