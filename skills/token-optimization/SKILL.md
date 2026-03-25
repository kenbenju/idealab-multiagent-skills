---
name: token-optimization
version: 3.0.0
description: |
  High-efficiency budget management system for long-context operations. 
  Uses semantic pruning, prompt compression, and batching logic to 
  reduce API costs by up to 60% while maintaining reasoning depth.
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Architecture & Infrastructure
trigger_phrases:
  - optimize token usage for this session
  - compress prompt while preserving logic
  - token budget audit for [Multi-Agent Swarm]
  - batch these requests into a single call
  - cost-efficiency pruning initialization
license: IDEALAB Partners v3.0
---

# 📉 Token Optimization & Budget Engine (v3.0 Semantic Compressor)

## 🗺️ Ontological Compression Map
```mermaid
graph TD
  A[Raw Comprehensive Prompt] --> B{Semantic Audit}
  B -->|Redundant| C[Lossless Compression]
  B -->|High Value| D[Reasoning Preservation]
  B -->|Noise| E[Hard Pruning]
  
  C & D & E --> F[Optimized Token Stream]
  F --> G[Execution]
  G --> H[Outcome vs Cost Analysis]
```

---

## 📥 Inputs & 📤 Outputs

### `<optimization_request>`
- **Active Context:** Current prompt/history.
- **Goal:** Specific outcome required.
- **Threshold:** (e.g., "Max 4,000 tokens per agent").

### `<compression_log_schema>`
```json
{
  "original_token_count": "int",
  "optimized_token_count": "int",
  "reduction_percentage": "float",
  "logic_integrity_score": "0-1.0",
  "methods_applied": ["keyword_distillation", "template_merging"]
}
```

---

## 🧬 Efficiency Protocols

### 1. Keyword Distillation (Semantics First)
Instead of repetitive instructions, use **Linguistic Anchors**:
- *Verbose:* "Please ensure that you do not use any words that are common in AI writing like 'delve' or 'comprehensive'."
- *Optimized:* `Negative-Pattern: [ai-buzzwords]`.

### 2. Multi-Agent Batching
Minimize the "System Message Overload". If 3 agents share 80% of the same brand data:
1. Create a **Shared Context Anchor**.
2. Call sub-agents with **Delta-Instructions** only.

### 3. Pruning the "Thinking" Budget
Claude 3.7 reasoning can be token-heavy.
- **Rule:** For simple tasks (e.g., generating 3 hashtags), limit `extended-thinking` to `budget: 512 tokens`.
- **Rule:** For complex strategy (e.g., full product launch), allow `budget: 16k tokens`.

### 4. Summarization Recursing
Every 10 interaction turns, Memory and Token-Opt MUST collaborate to:
1. Summarize the path taken.
2. Drop all previous raw turns from the active buffer.
3. Preserve only the `State Vector`.

---

## 🛠️ Usage Strategy
This skill should be called by the `orchestrator` as a **Pre-Processor**. Every prompt sent to a specialist must pass through the `token-optimization` filter first.

---

*© 2026 IDEALAB PARTNERS — Multi-Agent System*
