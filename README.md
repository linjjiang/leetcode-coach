# LeetCode Coach — Claude Code Skill

Interactive LeetCode coaching skill for Claude Code, tuned for MLE interview preparation.

## What It Does

Provides 8 structured coaching modes with invariant-first reasoning and ML connections:

| Mode | Trigger | Description |
|------|---------|-------------|
| **Debug** | `debug` | Incremental bug fixing without rewriting your solution |
| **Hint** | `hint` / `I'm stuck` | Pattern tag + one directional hint |
| **Complexity Check** | `complexity check` | Tests your complexity reasoning |
| **Optimize** | `optimize` | Optimality verdict with comparison table |
| **Walkthrough** | `walkthrough` | Mock interview with signal assessment |
| **Mistake Summary** | `summarize my mistakes` | Ranked mistakes with decision rules |
| **Notes** | `notes` / `flashcard` | Generates structured problem notes + updates tracker |
| **Code Templates** | `update templates` | Adds reusable code patterns to reference |

## Installation

Copy the skill into your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/leetcode-coach
cp -r . ~/.claude/skills/leetcode-coach/
```

On first activation, the skill automatically creates these files in your working directory (if missing):

- `notion-leetcode-template.md` — Notion database setup + page template
- `mistakes-log.md` — Recurring mistake patterns and session logs
- `problem-tracker.csv` — CSV tracker for solved problems
- `code-templates.md` — Reusable code pattern reference
- `problems/` — Directory for per-problem notes

## File Structure

```
leetcode-coach/
├── SKILL.md              # Skill definition (all modes + instructions)
├── README.md
└── references/           # Starter templates (copied on first use)
    ├── notion-leetcode-template.md
    ├── mistakes-log-template.md
    ├── problem-tracker-template.csv
    └── code-templates.md
```

## Core Principles

- **Invariant-first reasoning** — every explanation identifies the core invariant
- **Complexity is mandatory** — every solution includes time/space analysis with reasoning
- **Protect ownership** — guides toward insight, never hands over full solutions unprompted
- **Interview-grade communication** — frames reasoning as you'd speak to an interviewer
- **MLE connections** — relates problems to ML concepts when natural (edit distance <> NLP, topological sort <> computation graphs, etc.)
