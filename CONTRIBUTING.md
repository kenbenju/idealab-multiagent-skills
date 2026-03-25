# Contributing to IDEALAB Multi-Agent Skills

Thank you for your interest in contributing! To maintain the **10,000% logic** standard and the safety of our users, we follow a strict review policy.

## 🚨 The Approval-Only Rule
**All contributions MUST be approved by the IDEALAB Core Team.** We do not support "free" or unvetted merges to the main branch.

---

## Our Standards

### 1. The Skill Format (v2.0)
Every skill must contain a `SKILL.md` file with the following structure:
- **YAML Frontmatter:** Native Claude format (`name`, `description`, `trigger_phrases`).
- **🗺️ Ontological Map:** Clear logical flow of the agent's brain.
- **📥 Inputs & 📤 Outputs:** Standardized data schemas.
- **Detailed Step-by-Step:** Context-rich instructions.
- **Zero-Bias Check:** Must be compatible with the `anti-bias` skill.

### 2. Quality Audit
We review for:
- **Token Efficiency:** Does the skill use minimal tokens for maximum impact?
- **Tone Consistency:** Does it match the human-first tone of IDEALAB?
- **Modular Integrity:** Does it play well with other agents in the `orchestrator`?

---

## Contribution Workflow

1.  **Fork** the repository.
2.  **Branch:** Create a branch for your feature (`feat/new-skill-x`).
3.  **Draft:** Create your skill following the v2.0 template.
4.  **Self-Audit:** Run the `anti-bias` and `token-optimization` checks manually.
5.  **PR:** Submit a Pull Request with a detailed explanation of the business value.
6.  **Review:** An IDEALAB reviewer will provide feedback or request adjustments.
7.  **Merge:** Only an IDEALAB Maintainer can finalize the merge.

---

## ⚖️ Code of Conduct
Respect, clarity, and professionalism are mandatory. See `CODE_OF_CONDUCT.md`.

*© 2026 IDEALAB PARTNERS*
