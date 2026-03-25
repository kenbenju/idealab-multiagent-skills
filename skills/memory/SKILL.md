---
name: memory
version: 2.0.0
description: |
  Manages persistent context and structured memory across Claude sessions, agent calls,
  and long multi-step projects. Prevents context loss, repetition, and drift.
  Use this skill to store, retrieve, and summarize project memory between conversations.
  Produces: memory snapshots, context summaries, session logs, recall prompts.
  Trigger phrases: "remember this", "save context", "what did we decide",
  "session memory", "persistent context", "don't forget", "carry this forward"
claude_compatibility:
  - claude-3-5-sonnet
  - claude-3-7-sonnet
  - claude-code
marketplace_category: Architecture & Infrastructure
trigger_phrases:
  - remember this for later
  - save our context
  - what did we decide about this
  - carry this forward to the next session
  - session memory snapshot
  - don't lose this context
  - persistent memory for agents
license: IDEALAB Partners v2.0
author: IDEALAB PARTNERS <hello@idealabpartners.com>
---

> [!NOTE]
> **Claude Usage** — Claude does not have persistent memory between conversations by default. This skill provides a structured protocol for MANUALLY managing context continuity across sessions using structured snapshots, summaries, and recall prompts.

# 🧠 Memory Agent — Persistent Context & Session Continuity

## Objective

Give Claude persistent, structured memory across sessions by maintaining a living memory document that captures decisions, context, and outputs — and by providing precision recall prompts that re-inject context efficiently when a new session begins.

---

## Memory Architecture

```
MEMORY LAYERS (from fastest to deepest)

Layer 0: Working Memory (current session)
  → Claude's context window — active right now
  → Capacity: up to 200K tokens

Layer 1: Session Snapshot (end of session)
  → Structured summary saved by user in a file/notes
  → Injected at start of next session as a "memory prompt"
  → Size target: < 2,000 tokens

Layer 2: Project Memory (persistent across weeks)
  → Versioned memory document: `memory/[project-name].md`
  → Updated after every major milestone
  → Size target: < 5,000 tokens

Layer 3: Archive Memory (historical reference)
  → Full transcripts, earlier versions
  → Not injected — loaded on demand
```

---

## Step-by-Step Instructions

### Step 1 — Capture Working Decisions
Throughout any session, tag important decisions with `[MEMORY]`:

```
[MEMORY] Brand voice: warm, direct, anti-jargon. Never use "synergy".
[MEMORY] Target ICP: female founders, 30-45, LATAM, $5K-50K revenue.
[MEMORY] Preferred pricing tier: mid ($297 - $997).
[MEMORY] Avoid: passive voice, superlatives without data.
```

### Step 2 — Generate Session Snapshot (End of Session)
At the end of each working session, produce a compact snapshot:

```markdown
# Memory Snapshot — [Project Name]
Generated: [DATE TIME]
Session: #[N]

## What We Decided
- [Decision 1]
- [Decision 2]
- [Decision 3]

## Current State
- Stage: [e.g., "Brand DNA complete, starting copywriting"]
- Pending: [e.g., "Need client's logo files"]
- Next session goal: [e.g., "Write 3 email sequences"]

## Key Context (always inject)
- Brand: [name], [industry], [archetype]
- ICP: [name], [pain], [goal]
- Tone: [adjectives]
- Constraints: [word limits, platform rules, forbidden phrases]

## Agent Outputs Generated This Session
- `brand-dna`: [status: complete / draft / pending]
- `copywriting`: [status]
- `crm`: [status]
```

### Step 3 — Open New Session with Memory Recall Prompt
At the START of each new session, inject:

```
[MEMORY RECALL — [Project Name] — Session #[N+1]]

Continuing work on: [Project Name]
We are building: [1-sentence description]
Current stage: [where we left off]

Key decisions already made:
- [Decision 1]
- [Decision 2]

My ICP is: [compact ICP card]
Brand voice: [adjectives, forbidden words]

Today's goal: [specific task for this session]

Do not re-ask questions we've already answered. Resume from where we left off.
```

### Step 4 — Memory Versioning
Name memory files with semantic versions:
```
memory/
├── [project-name]-v1.0.md   ← Initial brand setup
├── [project-name]-v1.1.md   ← After campaign planning
├── [project-name]-v2.0.md   ← After product launch
```

### Step 5 — Cross-Agent Memory Sharing
When passing memory between agents in a multi-agent session, include only what's relevant per agent:

```
TO: copywriting agent
MEMORY INJECT: {icp, brand_voice, product_description, forbidden_phrases}
EXCLUDE: {crm_records, analytics_dashboards, contract_terms}
```

---

## Memory Commands for Claude

| Command | Action |
|---------|--------|
| `MEMORY SAVE` | Generate a session snapshot now |
| `MEMORY RECALL` | Re-inject the latest snapshot as context |
| `MEMORY STATUS` | Show what's in current working memory |
| `MEMORY CLEAR` | Declare a fresh start (new project) |
| `MEMORY DELTA` | Show only what changed since last snapshot |

---

## Integration Points
- **Used by**: Every agent (inject before starting any session)
- **Connects to**: `token-optimization` (compact memory = fewer tokens), `multi-agent` (shared state schema)

---

*© 2026 IDEALAB PARTNERS — For use with Claude (claude.ai) and Claude Code*
