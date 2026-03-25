---
name: Social Media Design Agent
version: 1.0.0
description: Generates platform-specific social media strategies including content calendars, caption writing, visual briefs, and hashtag research — always aligned to brand voice.
author: IDEALAB PARTNERS <hello@idealabpartners.com>
license: IDEALAB Partners v1.0
inputs:
  - name: brand_context
    type: object
    description: Brand DNA output (name, voice, colors, archetype, audience)
    required: true
  - name: campaign_goal
    type: string
    description: Primary goal (awareness, engagement, lead generation, sales)
    required: true
  - name: platforms
    type: array
    description: Target platforms (instagram, tiktok, linkedin, facebook, twitter/x, youtube)
    required: true
  - name: content_period
    type: string
    description: Period to plan (e.g. "30 days", "1 week", "campaign: Black Friday")
    required: false
  - name: product_or_service
    type: string
    description: What is being promoted
    required: false
outputs:
  - name: content_calendar
    type: object
    description: Day-by-day content plan with post type, topic, caption, hashtags, and visual brief
  - name: caption_set
    type: array
    description: Ready-to-use captions per platform with CTAs
  - name: visual_brief
    type: object
    description: Visual direction for designers (style, colors, mood, reference)
  - name: hashtag_strategy
    type: object
    description: Tiered hashtag sets per platform (niche, medium, broad)
agents_required:
  - brand-dna
tags:
  - social-media
  - content
  - marketing
  - design
---

# 📱 Social Media Design Agent

## Objective

Design a complete, deployment-ready social media strategy for a given brand, campaign, and platform set — from content calendar to individual post captions and visual briefs.

---

## Trigger

Activate when the user needs: content plans, captions, visual direction, or social media strategy.

---

## Step-by-Step Instructions

### Step 1 — Profile the Brand on Each Platform
For each target platform, define:
- **Optimal post frequency** (Instagram: 4-5x/week; LinkedIn: 3x/week; TikTok: daily; etc.)
- **Content formats available** (carousel, reel/video, static image, story, poll, article)
- **Tone calibration** (LinkedIn = professional + insightful; TikTok = casual + fast; Instagram = aesthetic + warm)

### Step 2 — Build the Content Pillars
Define 4-5 content pillars based on `campaign_goal` and `brand_context`:

| Pillar | Purpose | % of Content |
|--------|---------|--------------|
| Education | Position as expert | 30% |
| Inspiration | Emotional connection | 20% |
| Behind the Scenes | Build trust | 15% |
| Product/Offer | Drive conversion | 25% |
| Community/UGC | Engagement & loyalty | 10% |

### Step 3 — Generate Content Calendar
For each day in `content_period`, specify:
- Date & day of week
- Platform
- Content pillar
- Post format
- Topic / Hook (first 3 words)
- Caption (full text with CTA)
- Hashtags (15–30 for Instagram, 3–5 for LinkedIn, 5–10 for TikTok)
- Visual brief (2–3 sentences describing the image/video)

### Step 4 — Write Captions
For each post, write a caption that:
1. Opens with a strong **hook** (question, bold statement, or surprising fact)
2. Delivers **value** (tip, story, or insight) in 3–5 short paragraphs
3. Ends with a **CTA** (comment, save, DM, click link in bio)
4. Matches the brand's **tone of voice** exactly

### Step 5 — Design Visual Brief
For each post, describe:
- Color palette reference (use brand colors from `brand_context`)
- Layout type (centered, rule-of-thirds, full-bleed, text overlay)
- Mood/feel (minimalist, vibrant, dark, warm, editorial)
- Key visual element (person, product, icon, pattern, quote)
- Reference style (e.g., "Clean and minimal like Apple ads, dark background, white bold typography")

### Step 6 — Hashtag Strategy
Build 3 tiers per platform:
- **Niche** (< 50K posts): high relevance, low competition
- **Medium** (50K–500K posts): good reach potential
- **Broad** (> 500K posts): trending, high exposure but competitive

---

## Output Format

```json
{
  "content_calendar": [
    {
      "date": "2026-04-01",
      "platform": "instagram",
      "pillar": "Education",
      "format": "carousel",
      "topic": "5 errores que...",
      "caption": "¿Cuántas veces has...\n\n...\n\n👉 Guarda este post...",
      "hashtags": ["#marketing", "#emprendimiento"],
      "visual_brief": "Fondo blanco, tipografía bold negra, íconos minimalistas en cada slide."
    }
  ],
  "caption_set": [...],
  "visual_brief": { "palette": "#6C3BF5, #F5F0FF", "mood": "premium y cercano" },
  "hashtag_strategy": { "niche": [], "medium": [], "broad": [] }
}
```

---

## Integration Points

- **Receives from**: `brand-dna` (voice, palette, archetype), `digital-twin` (audience persona), `copywriting` (copy blocks)
- **Sends to**: `document-design` (to format as a PDF content calendar)

---

*© 2026 IDEALAB PARTNERS — Licensed under IDEALAB Partners v1.0*
