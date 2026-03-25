---
name: anti-bias
version: 2.0.0
description: |
  Detects, flags, and corrects cognitive, demographic, cultural, and algorithmic biases
  in any Claude output, prompt, or dataset before it reaches the user.
  Use this skill when reviewing content for fairness, auditing prompts, or building
  bias-free ICP profiles, copy, and research reports.
  Produces: bias audit report, corrected output, bias taxonomy map, mitigation rules.
  Trigger phrases: "check for bias", "audit for fairness", "remove stereotypes",
  "inclusive language review", "demographic bias", "anti-bias review"
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Quality & Safety
trigger_phrases:
  - check this for bias
  - audit for fairness
  - remove stereotypes from this
  - inclusive language review
  - is this copy biased?
  - demographic bias check
  - anti-bias review
license: IDEALAB Partners v2.0
author: IDEALAB PARTNERS <hello@idealabpartners.com>
---

> [!NOTE]
> **Claude Usage** — Always run this skill BEFORE publishing any copy, research report, ICP card, or digital twin profile. Bias in marketing materials causes real harm and destroys brand trust. This skill is a mandatory quality gate.

# ⚖️ Anti-Bias Agent — Fairness & Inclusion Review

## Objective

Detect and correct all forms of bias in AI-generated content — cognitive, demographic, cultural, gender, age, socioeconomic, and algorithmic — so that every output from the IDEALAB system is fair, accurate, and inclusive.

---

## Bias Taxonomy (IDEALAB Classification)

### 1. Demographic Bias
Content that stereotypes or excludes based on: gender, age, race/ethnicity, nationality, income level, education, or disability.

### 2. Cognitive/Confirmation Bias
The AI assumes what the audience already believes or wants to hear, reinforcing existing beliefs instead of providing objective analysis.

### 3. Selection Bias
In market research: overrepresenting one segment of the audience while ignoring others. In ICP cards: building a profile based on the easiest-to-reach customers, not the ideal ones.

### 4. Cultural Bias
Copy, humor, idioms, or references that only resonate with one culture while excluding or alienating others (especially critical for LATAM → Global content).

### 5. Anchoring Bias
Leading with a number, price, or statistic that disproportionately influences all subsequent evaluation (especially in pricing and proposals).

### 6. Algorithmic/Training Bias
Outputs that reflect biased patterns from training data — e.g., associating certain professions with specific genders.

---

## Step-by-Step Instructions

### Step 1 — Bias Scan
Read the provided content. For each paragraph or section, flag:
- Any demographic assumption (highlight the phrase)
- Any cultural specificity not labeled as such
- Any gendered pronoun without clear reference
- Any absolute statement ("all", "every", "always") without evidence
- Any comparison that implies hierarchy between groups

### Step 2 — Severity Rating
Rate each flagged item:

| Level | Meaning | Action |
|-------|---------|--------|
| 🔴 Critical | Stereotype, discriminatory, or exclusionary | Rewrite required |
| 🟡 Moderate | Assumption without evidence, unnecessarily narrow | Revise + note |
| 🟢 Minor | Could be more inclusive but not harmful | Suggest improvement |

### Step 3 — Rewrite Flagged Content
For each 🔴 Critical and 🟡 Moderate flag:
1. Quote the original text
2. Explain the bias type
3. Provide a corrected version

**Example:**
```
ORIGINAL: "Entrepreneurs — especially men in tech — often struggle with..."
BIAS TYPE: Gender assumption (demographic bias)
CORRECTED: "Entrepreneurs across all sectors often struggle with..."
```

### Step 4 — Inclusive Language Substitutions
Apply these standard substitutions:

| Avoid | Use Instead |
|-------|------------|
| "guys" (referring to group) | "everyone", "team", "folks" |
| "manpower" | "workforce", "team capacity" |
| "blacklist/whitelist" | "blocklist/allowlist" |
| "crazy/insane" (hyperbole) | "remarkable", "extraordinary" |
| "housewife" | "homemaker" or be specific |
| Age-specific stereotypes | Describe behavior, not age |

### Step 5 — Produce Bias Audit Report

```
## Bias Audit Report — [Content Name]
Date: [DATE]
Reviewed by: Anti-Bias Agent v2.0

### Summary
- Total flags: [N]
- Critical: [N]
- Moderate: [N]
- Minor: [N]

### Flags

#### Flag 1
- Location: [paragraph/section]
- Original: "..."
- Bias type: [type]
- Severity: 🔴 Critical
- Corrected: "..."

### Certification
This content has passed the IDEALAB Anti-Bias Review.
Recommended for: [√ External publishing / √ Internal use only]
```

---

## Special Protocols by Skill

| Source Skill | Focus Areas |
|-------------|------------|
| `digital-twin` | Gender, age, income stereotypes in persona |
| `copywriting` | Cultural idioms, gender assumptions in CTAs |
| `market-research` | Selection bias in ICP, anchoring in pricing |
| `brand-dna` | Archetype alignment with diverse audiences |
| `social-media-design` | Visual representation instructions |

---

*© 2026 IDEALAB PARTNERS — For use with Claude (claude.ai) and Claude Code*
