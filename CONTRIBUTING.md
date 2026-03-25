# Contributing to IDEALAB PARTNERS Multi-Agent Skills

Thank you for your interest in contributing! This guide will help you get started.

---

## 🚀 Quick Start

```bash
# 1. Fork and clone the repository
git clone https://github.com/<your-username>/idealab-multiagent-skills.git
cd idealab-multiagent-skills

# 2. Create a feature branch
git checkout -b feat/your-skill-name

# 3. Make your changes and commit
git add .
git commit -m "feat(skill-name): brief description of change"

# 4. Push and open a Pull Request
git push origin feat/your-skill-name
```

---

## 📁 Skill Structure

Every skill lives in `skills/<skill-name>/` and must follow this structure:

```
skills/your-skill/
├── SKILL.md           ← Required: main instruction file (see template below)
├── examples/
│   └── example_01.md  ← At least one working example
└── resources/         ← Optional: templates, diagrams, reference files
    └── .gitkeep
```

### SKILL.md Frontmatter Template

```yaml
---
name: Your Skill Name
version: 1.0.0
description: One-sentence description of what this skill does.
author: Your Name <email@example.com>
license: IDEALAB Partners v1.0
inputs:
  - name: input_field
    type: string
    description: What this input is for
    required: true
outputs:
  - name: output_field
    type: string
    description: What this output contains
agents_required:
  - orchestrator
tags:
  - marketing
  - automation
---
```

---

## ✅ Pull Request Checklist

Before submitting a PR, ensure:

- [ ] `SKILL.md` contains valid YAML frontmatter
- [ ] At least one example in `examples/` demonstrates the skill end-to-end
- [ ] Skill name in frontmatter matches the folder name
- [ ] No sensitive data (API keys, passwords) is included
- [ ] Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `refactor:`
- [ ] You have read the [Code of Conduct](CODE_OF_CONDUCT.md)

---

## 🐛 Reporting Bugs

Use the **Bug Report** issue template. Include:
- Skill name and version
- Expected vs actual behavior
- Minimal reproduction steps

## 💡 Proposing New Skills

Use the **Feature Request** issue template. Describe:
- Problem the skill solves
- Target inputs and outputs
- Which existing skills it integrates with

---

## 📜 License Agreement

By contributing, you agree your contributions are licensed under the [IDEALAB PARTNERS License](LICENSE).

---

© 2026 IDEALAB PARTNERS
