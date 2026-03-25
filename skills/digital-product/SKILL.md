---
name: Digital Product Creation Agent
version: 1.0.0
description: Defines, scopes, and structures digital products including eBooks, online courses, template packs, memberships, and SaaS concepts — from idea to launch-ready specification.
author: IDEALAB PARTNERS <hello@idealabpartners.com>
license: IDEALAB Partners v1.0
inputs:
  - name: product_idea
    type: string
    description: Raw idea or problem the product solves
    required: true
  - name: target_audience
    type: object
    description: ICP card or persona (from market-research or digital-twin)
    required: true
  - name: product_type
    type: string
    description: "ebook, online_course, template_pack, membership, saas_mvp, workshop, masterclass"
    required: true
  - name: price_range
    type: string
    description: "Expected price tier: low (< $50), mid ($50-$300), high ($300-$2000), ultra ($2000+)"
    required: false
  - name: brand_context
    type: object
    description: Brand DNA output for naming and positioning
    required: false
outputs:
  - name: product_spec
    type: object
    description: Complete product specification (name, tagline, description, format, delivery)
  - name: content_outline
    type: array
    description: Full table of contents or module/lesson structure
  - name: pricing_strategy
    type: object
    description: Pricing tiers, bonuses, and launch pricing rationale
  - name: launch_plan
    type: object
    description: Pre-launch, launch, and post-launch action sequence
  - name: sales_assets_needed
    type: array
    description: List of copy and design assets needed to sell this product
agents_required:
  - market-research
  - copywriting
  - brand-dna
tags:
  - digital-product
  - elearning
  - ebook
  - saas
  - launch
---

# 🚀 Digital Product Creation Agent

## Objective

Transform a raw idea into a fully specified, launch-ready digital product — with structure, pricing, and a complete asset list so you can move from concept to market without guesswork.

---

## Step-by-Step Instructions

### Step 1 — Product Discovery
Answer the 5 foundational questions:
1. **What problem does this solve?** (Be brutally specific)
2. **Who experiences this problem most acutely?** (ICP alignment)
3. **What does success look like for the buyer?** (Transformation promise)
4. **Why is this product the best vehicle for that transformation?**
5. **Why now?** (Market timing or urgency factor)

### Step 2 — Product Naming and Positioning
Generate 3 name options following this formula:
`[Adjective] + [Method/System] + [Result]`

Examples:
- "The Visibility Blueprint" (course for coaches)
- "Revenue OS" (template pack for businesses)
- "The Brand DNA Kit" (eBook + worksheets)

Write a one-line tagline per option:
`[Product Name] — [What it does] so you can [desired outcome] without [common objection].`

### Step 3 — Content / Module Structure

**For eBooks:**
```
- Introduction (Problem + Promise)
- Chapter 1: Foundation
- Chapter 2–N: Core method (1 concept per chapter)
- Final Chapter: Implementation roadmap
- Appendix: Worksheets, templates, resources
```

**For Online Courses:**
```
Module 0: Welcome + How to use this course
Module 1: Foundation (mindset/context)
Module 2–N: Core skills or frameworks
Module X: Implementation + live practice
Bonus Module: Advanced / community / Q&A
```

**For Template Packs:**
```
- Template 1: [Name] — describes what it is and when to use it
- Template 2: ...
- User guide PDF
- Video walkthrough (optional)
```

### Step 4 — Pricing Strategy

| Tier | Price | What's included | Target buyer |
|------|-------|----------------|--------------|
| Core | $X | Base product only | DIY audience |
| Pro | $X + $Y | Core + templates + workbooks | Serious implementers |
| VIP | $X + $Y + $Z | Pro + 1:1 call or group access | Premium |

Set launch price at 40-60% of full price with urgency window (72h – 7 days).

### Step 5 — Launch Plan
```
PRE-LAUNCH (2-4 weeks before):
- Waitlist page live
- Social media teaser content (3 posts/week)
- Behind-the-scenes stories
- Email to existing list: "Something is coming"

LAUNCH WEEK:
- Day 1: Doors open — announcement post + email
- Day 2: Case study / transformation story
- Day 3: FAQ post
- Day 4: Testimonial or early buyer result
- Day 5: Last 48h warning
- Day 6: Last 24h warning + bonus reminder
- Day 7: Cart closes — final email

POST-LAUNCH:
- Thank you email + access delivery
- Onboarding sequence
- Review request at day 7 and day 30
- Upsell to next tier or related product
```

### Step 6 — Sales Asset List
Based on product type, list all assets needed:
- Sales page (long-form)
- Checkout page
- Email sequence (pre-launch + launch)
- Social media graphics (announcement, countdown, testimonials)
- Lead magnet or freebie (list builder)
- Video sales letter (VSL) script (if applicable)

---

## Integration Points

- **Receives from**: `market-research` (validated problem), `digital-twin` (audience language), `brand-dna` (naming and positioning)
- **Sends to**: `copywriting` (sales page, emails), `social-media-design` (launch content), `document-design` (product PDF/deck)

---

*© 2026 IDEALAB PARTNERS — Licensed under IDEALAB Partners v1.0*
