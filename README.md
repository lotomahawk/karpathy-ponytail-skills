# karpathy-ponytail-skills

A single `CLAUDE.md` merging Andrej Karpathy's LLM coding guidelines with Ponytail's laziness ladder, for use with Claude Code and other AI coding agents.

---

## Why

Karpathy identified the core failure modes:

> "The models make wrong assumptions on your behalf and just run along with them without checking. They don't manage their confusion, don't seek clarifications, don't surface inconsistencies, don't present tradeoffs, don't push back when they should."

> "They really like to overcomplicate code and APIs, bloat abstractions, don't clean up dead code... implement a bloated construction over 1000 lines when 100 would do."

> "They still sometimes change/remove comments and code they don't sufficiently understand as side effects, even if orthogonal to the task."

Ponytail added the concrete decision ladder Karpathy's simplicity rule was missing:

> "The best code is the code never written. Stop at the first rung that holds: does this need to exist at all? Already in the codebase? Stdlib? Native platform? Existing dependency? One line? Only then: minimum code that works."

This repo merges both into one file.

---

## What's inside

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Drop into any project root — Claude Code loads it automatically |
| `AGENTS.md` | Same content — for Codex, OpenCode, and agents that read `AGENTS.md` |
| `skills/karpathy-ponytail/SKILL.md` | Claude Code plugin skill with frontmatter |
| `.cursor/rules/karpathy-ponytail.mdc` | Cursor project rule — always-on |

---

## Install

**Option 1 — Copy into your project (one project):**
```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/AbdullahHameedKhan/karpathy-ponytail-skills/main/CLAUDE.md
```

**Option 2 — Append to an existing CLAUDE.md:**
```bash
echo "" >> CLAUDE.md
curl https://raw.githubusercontent.com/AbdullahHameedKhan/karpathy-ponytail-skills/main/CLAUDE.md >> CLAUDE.md
```

**Option 3 — Claude Code plugin (all projects):**

Inside a Claude Code session:
```
/plugin marketplace add AbdullahHameedKhan/karpathy-ponytail-skills
/plugin install karpathy-ponytail@karpathy-ponytail
```

---

## The five principles

1. **Think Before Coding** — surface tradeoffs, ask before assuming, name confusion
2. **Simplicity — The Ladder** — 7-rung decision ladder from YAGNI to minimum working code
3. **Surgical Changes** — touch only what you must, clean up only your own mess
4. **Bug Fixes** — root cause not symptom, grep all callers, fix the shared function once
5. **Goal-Driven Execution** — define success criteria, loop until verified

---

## Sources

- Andrej Karpathy's observations on LLM coding pitfalls
- [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) — MIT License
