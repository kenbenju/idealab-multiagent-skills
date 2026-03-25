---
name: CRM Agent
version: 1.0.0
description: Manages customer relationship data including contact ingestion, interaction logging, pipeline stage tracking, follow-up automation sequences, and contact history traces.
author: IDEALAB PARTNERS <hello@idealabpartners.com>
license: IDEALAB Partners v1.0
inputs:
  - name: contact_data
    type: object
    description: Raw contact information (name, email, phone, company, source)
    required: true
  - name: interaction_log
    type: array
    description: List of past interactions (date, channel, summary, outcome)
    required: false
  - name: pipeline_stage
    type: string
    description: Current pipeline stage (lead, prospect, qualified, proposal, negotiation, closed-won, closed-lost)
    required: false
  - name: follow_up_goal
    type: string
    description: Goal of next follow-up (nurture, convert, upsell, reactivate)
    required: false
outputs:
  - name: crm_record
    type: object
    description: Structured CRM contact card with full history, score, and tags
  - name: pipeline_update
    type: object
    description: Updated pipeline stage with reasoning and recommended next action
  - name: follow_up_sequence
    type: array
    description: Automated follow-up messages (email/WhatsApp) with timing and personalization
  - name: contact_trace
    type: array
    description: Full chronological interaction history for this contact
agents_required:
  - orchestrator
tags:
  - crm
  - sales
  - contacts
  - automation
  - follow-up
---

# 📋 CRM Agent — Contact Tracking & Relationship Management

## Objective

Maintain a complete, structured record of every contact interaction, advance contacts through the sales pipeline intelligently, and generate personalized follow-up sequences that feel human.

---

## Trigger

Activate when a new contact is added, an interaction occurs, a pipeline stage needs updating, or a follow-up sequence is required.

---

## Step-by-Step Instructions

### Step 1 — Ingest and Enrich Contact Data
Create a structured contact card:

```
## Contact Card

### Basic Info
- Full Name:
- Email:
- Phone / WhatsApp:
- Company / Role:
- Location:
- Source (how they found us): [Referral, Instagram, LinkedIn, Website, Event, Cold Outreach]

### Tags
- Industry:
- ICP Match: [High / Medium / Low]
- Language:
- Pain Points (from conversation):

### Lead Score (0–100)
- Score:
- Scoring factors: [Budget, Authority, Need, Timeline — BANT]
```

### Step 2 — Log Interaction History
For each interaction, record:

| Field | Value |
|-------|-------|
| Date & Time | |
| Channel | Email / WhatsApp / Call / DM / Meeting / Event |
| Direction | Inbound / Outbound |
| Summary | 2-3 sentence description of what was discussed |
| Sentiment | Positive / Neutral / Negative |
| Commitment made | Any promises or next steps agreed |
| Next action | What should happen next and by when |

### Step 3 — Assign Pipeline Stage
Evaluate contact against pipeline criteria:

| Stage | Criteria |
|-------|----------|
| **Lead** | Showed initial interest, no qualification yet |
| **Prospect** | Confirmed pain point alignment, exploring options |
| **Qualified** | Budget, authority, need, and timeline confirmed |
| **Proposal** | Formal offer sent |
| **Negotiation** | Active back-and-forth on terms |
| **Closed-Won** | Deal signed / payment received |
| **Closed-Lost** | Deal lost — document reason |

Provide reasoning for stage assignment and recommended next action.

### Step 4 — Generate Follow-Up Sequence
Based on `follow_up_goal`, generate a sequence of 3–5 touchpoints:

For each touchpoint:
- **Day**: When to send (relative to last contact)
- **Channel**: Email, WhatsApp, LinkedIn DM, Phone
- **Subject/Hook**: Opening line
- **Message**: Full personalized message (human tone, no corporate speak)
- **CTA**: Single clear call to action

#### Human Tone Rules for Follow-Ups:
- Write as a real person, not a company
- Reference specific details from the last interaction
- Keep messages short (under 150 words for messages, 250 for emails)
- Use the contact's first name naturally
- Never use: "I hope this email finds you well", "Per my last email", "Circle back"

### Step 5 — Build Contact Trace
Produce a full chronological timeline of all interactions, sorted from newest to oldest, with tags for sentiment and outcome.

---

## Output Format

```json
{
  "crm_record": {
    "contact_id": "IDEALAB-2026-001",
    "name": "María González",
    "email": "maria@empresa.com",
    "pipeline_stage": "qualified",
    "lead_score": 82,
    "tags": ["coach", "high-icp", "warm"],
    "last_contact": "2026-03-20"
  },
  "pipeline_update": {
    "previous_stage": "prospect",
    "new_stage": "qualified",
    "reason": "Confirmed budget and decision-making authority",
    "next_action": "Send proposal by March 27"
  },
  "follow_up_sequence": [
    {
      "day": 1,
      "channel": "whatsapp",
      "message": "Hola María, fue un gusto hablar hoy...",
      "cta": "¿Te parece bien el jueves a las 3pm para revisar la propuesta?"
    }
  ],
  "contact_trace": [
    { "date": "2026-03-20", "channel": "call", "summary": "...", "sentiment": "positive" }
  ]
}
```

---

## Integration Points

- **Receives from**: `orchestrator`, external forms, WhatsApp bots, website lead magnets
- **Sends to**: `copywriting` (for personalized message tone), `document-design` (CRM reports), `digital-twin` (for persona enrichment)

---

*© 2026 IDEALAB PARTNERS — Licensed under IDEALAB Partners v1.0*
