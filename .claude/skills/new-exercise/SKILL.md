---
name: new-exercise
description: Scaffold a new practical-exercise folder under exercises/ for the Intro to Data Engineering course. Use when the user starts a new course exercise, lab, or hands-on assignment, or says "/new-exercise", "new exercise", "start exercise".
---

# New exercise scaffold

Create a standardized folder for a course exercise.

## Steps

1. Determine the next sequence number: list `exercises/` and take the highest `NN-` prefix + 1 (start at `01` if empty).
2. Ask the user (only if not given in their message): which module/topic is this exercise about, and what does it ask you to do?
3. Create `exercises/NN-short-kebab-name/` with:
   - `README.md` using the template below
   - `src/` (empty, add `.gitkeep`)
   - `data/` (empty, add `.gitkeep`)
4. If the exercise needs a Python environment, use `uv` (`uv init`, `uv add ...`) inside the exercise folder rather than a repo-wide venv.
5. Do NOT commit automatically — the user commits when the exercise is done.

## README template

```markdown
# NN — <Exercise title>

**Module:** <course module/week>
**Date started:** <YYYY-MM-DD>

## Task

<what the exercise asks, in 2-4 sentences>

## Approach & decisions

<key decisions and why — written as the work happens>

## Outcome

<what was built/learned; filled in at the end>
```

## After finishing an exercise

Remind the user to run `/log-learning` so the knowledge base stays current.
