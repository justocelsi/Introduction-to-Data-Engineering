# Introduction to Data Engineering

Personal learning repo for the Coursera course [Introduction to Data Engineering](https://www.coursera.org/learn/intro-to-data-engineering).

Goal: level up from junior data scientist to data engineer — solid fundamentals plus the tooling needed to eventually build a chatbot over our own data.

## Structure

```
exercises/          one folder per practical exercise: NN-short-name/
docs/knowledge.html running knowledge base — concepts, tools, and takeaways per module
.claude/skills/     project skills that automate the workflow (see below)
```

## Workflow (Claude Code skills)

- `/new-exercise` — scaffolds a new folder under `exercises/` with a standard layout (README, src, data).
- `/log-learning` — appends what was just learned (concepts, tools, gotchas) to `docs/knowledge.html`.

Open `docs/knowledge.html` in a browser to review everything learned so far.

## Progress

| Module | Topic | Status | Logged |
|---|---|---|---|
| 1 | The data engineering lifecycle, undercurrents, history of the field | ✅ done | 2026-07-11 |

Reference books read alongside the course (local only, not in git): *Fundamentals of Data Engineering* (Reis & Housley) and *Designing Data-Intensive Applications* (Kleppmann).

## Exercise naming

`exercises/01-module-name-topic/` — two-digit sequence, kebab-case, short.

Each exercise folder contains:

- `README.md` — what the exercise asks, decisions made, outcome
- `src/` — code
- `data/` — small sample data only (large/raw data stays out of git)
