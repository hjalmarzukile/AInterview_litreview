---
name: open-issue
level: s1
description: Use when starting any new piece of work — research question, task, future direction, or identified gap. Every commit must trace back to an issue.
---

# Skill: Open an issue

## When to use
Before any work begins. If you cannot point to an issue, do not commit.

## Steps

1. **Check for duplicates** — search open issues for similar questions before creating a new one

2. **Choose the right label**
   - `question` — an open research question needing investigation
   - `task` — a concrete piece of work with a clear output
   - `future-work` — a direction to pursue later, not now
   - `blocked` — waiting on something external
   - `bug` — something broken in code, data, or a skill

3. **Write the issue title as a question or clear action**
   - Good: `What is the effect of X on Y in cohort Z?`
   - Good: `Preprocess wave 3 survey data`
   - Bad: `Analysis` / `Work on paper`

4. **Issue body must include**
   - What question is being resolved, or what output is expected
   - Any relevant prior issues (use `#N` references)
   - If personal data is involved: note `⚠️ MANUAL REQUIRED — personal data`

5. **Assign to the right person or agent**

6. **Link to a milestone** if the issue belongs to a deliverable (paper, report, release)

## Commit when done
Issues are not committed — they live in GitHub.
The commit that resolves the issue closes it via `closes #N` in the message.
