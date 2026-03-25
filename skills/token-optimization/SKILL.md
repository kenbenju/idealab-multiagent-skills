---
name: token-optimization
version: 2.0.0
description: |
  Minimizes token consumption across all Claude sessions and agent pipelines without
  losing output quality. Compresses prompts, summarizes context, batches requests,
  and implements progressive loading to maximize value per API dollar.
  Produces: optimized prompts, compression ratios, token audits, batching plans.
  Trigger phrases: "reduce tokens", "optimize prompt", "too long context",
  "save on API costs", "compress this prompt", "token budget", "context too large"
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Architecture & Infrastructure
trigger_phrases:
  - reduce token usage
  - optimize this prompt
  - my context is too large
  - save on API costs
  - compress this prompt
  - token budget management
  - context window is filling up
license: IDEALAB Partners v2.0
author: IDEALAB PARTNERS <hello@idealabpartners.com>
---

> [!NOTE]
> **Claude Usage** — Apply this skill BEFORE running multi-agent pipelines or long sessions. A 40-60% token reduction is routinely achievable without quality loss. Run token audits at the start of complex projects.

# ⚡ Token Optimization Agent — Efficiency Without Compromise

## Objective

Maximize the value of every token by compressing prompts, summarizing context, batching requests intelligently, and implementing progressive loading — while maintaining 100% output quality.

---

## Token Optimization Principles

1. **Compress, don't truncate** — Remove redundancy, not meaning
2. **Structure beats prose** — Tables and bullets use 30-50% fewer tokens than paragraphs
3. **Reference, don't repeat** — Point to earlier output instead of pasting it
4. **Delay loading** — Load skill files and references only when triggered
5. **Batch similar tasks** — Run variations in one prompt, not several
6. **Use examples sparingly** — One strong example > three weak ones

---

## Step-by-Step Instructions

### Step 1 — Token Audit
Before starting any session, estimate the token budget:

```
Token Audit — [Project Name]

Model: Claude 3.7 Sonnet (200K context window)
Target usage: < 150K (75%) — leave 25% buffer

Planned inputs:
- System prompt (CLAUDE.md):   ~2,000 tokens
- Memory snapshot:             ~1,500 tokens
- Active skill files (avg 3):  ~6,000 tokens
- User inputs per turn:        ~500 tokens × [N turns]
- Agent outputs:               ~1,000 tokens × [N agents]

TOTAL ESTIMATE: [X] tokens
STATUS: [OK / WARNING / CRITICAL]
```

### Step 2 — Prompt Compression Techniques

#### Technique 1: Remove Politeness Overhead
```
BEFORE (47 tokens):
"Could you please help me by writing a detailed, comprehensive email that
clearly communicates the value proposition of our new product?"

AFTER (18 tokens):
"Write a value proposition email for [product]. Tone: [X]. Goal: [Y]."
```

#### Technique 2: Replace Prose with Structure
```
BEFORE (prose, 80 tokens):
"The brand should feel warm and approachable but also professional and
expert. It should never feel corporate or cold. It should use contractions
and speak directly to the reader."

AFTER (structured, 32 tokens):
Brand voice: warm, approachable, expert
Never: corporate, cold, jargon
Always: contractions, direct address
```

#### Technique 3: Variable Substitution
Define once, reference everywhere:
```
[ICP] = "Female founder, 30-42, LATAM, health/wellness, $5-50K revenue"
[BRAND] = "IDEALAB, archetype: Sage + Creator, voice: direct+warm"
[GOAL] = "Sell $497 digital course launch"

Now use: "Write copy for [GOAL] targeting [ICP] with [BRAND] voice."
Instead of repeating all context each time.
```

#### Technique 4: Progressive Disclosure for Skills
Load skills in stages:
```
Stage 1 (always loaded): skill description (~100 tokens)
Stage 2 (load if relevant): full SKILL.md body (~2,000 tokens)
Stage 3 (load on demand): examples/ and resources/ files
```

#### Technique 5: Output Length Control
Add explicit length constraints to every prompt:
```
"Max output: 500 words"
"Return JSON only, no prose"
"Bullet list, max 10 items, max 15 words per item"
"Headline only, no explanation"
```

### Step 3 — Batch Request Design
Instead of 5 separate calls, batch:

```
INEFFICIENT (5 calls × 2,000 tokens each = 10,000 tokens):
Call 1: Write Instagram caption
Call 2: Write LinkedIn caption
Call 3: Write Twitter/X caption
Call 4: Write Facebook caption
Call 5: Write TikTok hook

OPTIMIZED (1 call × 3,000 tokens = 70% saving):
"Adapt this caption for: Instagram (150 words, 3 hashtags),
LinkedIn (200 words, professional tone), Twitter/X (280 chars, 1 CTA),
Facebook (100 words, conversational), TikTok hook (first 3 seconds).

Base caption: [CAPTION]
Brand: [BRAND VOICE]"
```

### Step 4 — Context Rotation Strategy
For very long sessions, rotate context:

```
Every 10 turns, run:
"Summarize our conversation so far in < 500 words, keeping:
- All decisions made
- Current task state
- Next steps
Then clear and restart with this summary as context."
```

### Step 5 — Token Budget per Agent (Multi-Agent Sessions)

```
Agent               Input Budget   Output Budget   Total
orchestrator        1,000          500             1,500
brand-dna           3,000          4,000           7,000
market-research     5,000          5,000           10,000
digital-twin        3,000          4,000           7,000
copywriting         4,000          6,000           10,000
social-media        3,000          4,000           7,000
crm                 2,000          2,000           4,000
document-design     3,000          3,000           6,000
[other agents]      2,000          2,000           4,000 each
─────────────────────────────────────────────────────────
TOTAL (9 agents)                                  ~70,000
Buffer (30%)                                      ~21,000
GRAND TOTAL                                       ~91,000 / 200,000
```

---

## Quick Reference: Token Counts for IDEALAB Skills

| Skill | Approx Tokens (SKILL.md) |
|-------|-------------------------|
| orchestrator | 2,800 |
| multi-agent | 2,600 |
| brand-dna | 3,200 |
| copywriting | 2,900 |
| digital-twin | 3,100 |
| [other skills] | ~2,500 avg |

---

*© 2026 IDEALAB PARTNERS — For use with Claude (claude.ai) and Claude Code*
