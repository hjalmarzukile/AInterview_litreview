---
name: manual-required
level: s1
description: Use when a task involves personal data, sensitive information, or anything that must not reach an external API. Stops agent execution and hands off to a human via a structured log.
---

# Skill: Manual required

## When to use
Immediately when you identify that a task involves:
- Personal identifiers (names, IDs, emails, health data)
- Sensitive institutional data
- Anything that should not leave the local machine
- Anything that should not be sent to an external API

Do not attempt the task. Do not send any data to the API.
Stop and execute this skill instead.

## Steps

### 1. Create the log file
Path: `logs/manual/YYYY-MM-DD_HH-MM_<task-name>.md`

Content:
```markdown
# MANUAL REQUIRED
date: YYYY-MM-DD HH:MM
issue: #N
task: <short description>

## What needs to be done
<clear step-by-step instructions for the human>

## Why this cannot be automated
<reason>

## Input files
- path/to/input/file

## Expected output
<what file to produce, where to put it, what commit to make>

## Resume
Once complete, close issue #N with commit referencing this log.
```

### 2. Commit the log
```
git add logs/manual/YYYY-MM-DD_HH-MM_task-name.md
git commit -m "log: manual required — <task> — see #N"
```

### 3. Open or update the GitHub issue
Add a comment to the issue:
```
⚠️ MANUAL REQUIRED

This task involves personal data and cannot be completed by the agent.
See logs/manual/YYYY-MM-DD_HH-MM_task-name.md for instructions.

Assigned to: <human researcher>
```

Add label `manual-required` to the issue.

### 4. Stop
Do not proceed with the original task.
The human will complete it locally and commit the result.

## After the human completes the task
The human:
1. Completes the work locally (no API calls)
2. Verifies output contains no raw personal data
3. Commits the output: `data(scope): <description> — closes #N`
4. Removes the `manual-required` label and closes the issue
