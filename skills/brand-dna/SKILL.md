---
name: Brand DNA Agent
version: 1.0.0
description: Creates a comprehensive Brand DNA canvas including mission, vision, values, brand archetype, voice and tone guide, visual identity system, and positioning statement.
author: IDEALAB PARTNERS <hello@idealabpartners.com>
license: IDEALAB Partners v1.0
inputs:
  - name: brand_name
    type: string
    description: The name of the brand
    required: true
  - name: industry
    type: string
    description: Industry or market the brand operates in
    required: true
  - name: founder_story
    type: string
    description: Brief origin story or "why we started" narrative
    required: false
  - name: target_audience
    type: object
    description: ICP card or persona description
    required: false
  - name: competitors
    type: array
    description: Main competitors (for differentiation mapping)
    required: false
  - name: keywords
    type: array
    description: Words that should describe the brand feeling (e.g. "bold", "warm", "expert", "playful")
    required: false
outputs:
  - name: brand_dna_canvas
    type: object
    description: Complete Brand DNA canvas (mission, vision, values, purpose, archetype, personality)
  - name: voice_guide
    type: object
    description: Detailed tone of voice guide with examples, forbidden phrases, and platform adaptations
  - name: visual_identity_system
    type: object
    description: Color palette, typography, logo direction, imagery style, and visual rules
  - name: positioning_statement
    type: string
    description: Single-sentence brand positioning statement
  - name: brand_story
    type: string
    description: 150-200 word brand story for About pages, pitches, and social bios
agents_required:
  - market-research
tags:
  - brand
  - identity
  - strategy
  - design
  - positioning
---

# 🧬 Brand DNA Agent

## Objective

Build the complete genetic code of a brand — the foundational layer from which all communication, design, and strategy must flow. A strong Brand DNA makes every future decision faster and more consistent.

---

## Step-by-Step Instructions

### Step 1 — Define the Brand Core

```
PURPOSE (Why it exists beyond making money)
"We exist to ________________________________."

MISSION (What we do, for whom, and how)
"We help [audience] achieve [outcome] through [method]."

VISION (The world we're working to create)
"A world where ________________________________."

VALUES (3-5 non-negotiable principles)
1. [Value]: [1-sentence definition and how it shows up in behavior]
2.
3.
```

### Step 2 — Choose Brand Archetype
Select the primary archetype (and an optional secondary):

| Archetype | Core Desire | Voice Feel | Examples |
|-----------|------------|------------|---------|
| The Hero | Mastery | Bold, inspiring | Nike, Duolingo |
| The Sage | Knowledge | Trusted, expert | Google, TED |
| The Creator | Innovation | Visionary, original | Apple, Lego |
| The Ruler | Control | Authoritative, premium | Rolex, Mercedes |
| The Caregiver | Service | Warm, nurturing | Dove, Johnson's |
| The Explorer | Freedom | Adventurous, free | Patagonia, Jeep |
| The Rebel | Revolution | Disruptive, raw | Harley-Davidson |
| The Magician | Transformation | Mysterious, inspiring | Disney, Tesla |
| The Lover | Connection | Sensual, intimate | Victoria's Secret |
| The Jester | Joy | Playful, witty | Old Spice, Skittles |
| The Everyman | Belonging | Relatable, down-to-earth | IKEA, Target |
| The Innocent | Goodness | Simple, pure, optimistic | Dove, Whole Foods |

State: **Primary Archetype** + **Secondary Archetype** + how they blend.

### Step 3 — Brand Personality and Voice

Define 5 personality traits on a spectrum:

| Trait | ←——— Scale ———→ | Trait |
|-------|-----------------|-------|
| Formal | ●○○○○ | Casual |
| Serious | ○○●○○ | Playful |
| Traditional | ○○○●○ | Innovative |
| Exclusive | ○●○○○ | Accessible |
| Reserved | ○○○○● | Expressive |

### Step 4 — Voice and Tone Guide

```
## Brand Voice — [Brand Name]

### We Are:
- [Adjective 1]: [1 sentence description] ✅ Example: "..."
- [Adjective 2]: [1 sentence description] ✅ Example: "..."
- [Adjective 3]: [1 sentence description] ✅ Example: "..."

### We Are NOT:
- ❌ [Adjective]: [1 sentence explaining what we avoid]
- ❌ [Adjective]: ...

### Platform Adaptations:
- Instagram: [tone adjustment, e.g., "warmer, more personal"]
- LinkedIn: [tone adjustment, e.g., "more professional, thought-leadership"]
- Email: [tone adjustment, e.g., "conversational but structured"]
- Website: [tone adjustment, e.g., "clear, benefit-driven, no jargon"]

### Always / Never List:
ALWAYS: Use active voice, short sentences, contractions (it's, we're), specific examples
NEVER: Use passive voice, industry jargon, generic superlatives ("best", "leading"), corporate speak
```

### Step 5 — Visual Identity System

```json
{
  "color_palette": {
    "primary": "#6C3BF5",
    "secondary": "#F5F0FF",
    "accent": "#FFB800",
    "neutrals": ["#1A1A2E", "#F8F8F8"],
    "usage_rules": "Primary on CTAs and headers; accent sparingly for emphasis only"
  },
  "typography": {
    "heading_font": "Inter Bold",
    "body_font": "Inter Regular",
    "accent_font": "Playfair Display (for pull quotes only)",
    "scale": "H1: 48px, H2: 36px, H3: 24px, Body: 16px, Caption: 13px"
  },
  "logo_direction": {
    "style": "Wordmark with geometric monogram",
    "clearspace": "Minimum 1x logo height on all sides",
    "forbidden_uses": ["Stretched", "Rotated", "Low contrast", "Drop shadow"]
  },
  "imagery_style": {
    "photography": "Real people, natural light, candid moments — no stock photo clichés",
    "illustration": "Clean geometric, brand color palette only",
    "video": "Handheld feel, documentary style, human stories"
  }
}
```

### Step 6 — Positioning Statement and Brand Story

**Positioning:**
`For [ICP], [Brand Name] is the [category] that [unique benefit] because [reason to believe].`

**Brand Story (150-200 words):**
Write a narrative that follows: Problem → Turning Point → Solution → Invitation.
Use first-person plural ("we") or the founder's voice. End with a direct invitation to the reader.

---

## Integration Points

- **Always runs before**: `copywriting`, `social-media-design`, `digital-product`
- **Receives from**: `market-research` (positioning context, competitor landscape)
- **Sends to**: All other agents (brand context is the foundation for every output)

---

*© 2026 IDEALAB PARTNERS — Licensed under IDEALAB Partners v1.0*
