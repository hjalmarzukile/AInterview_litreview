---
name: issue-triage
level: s3
description: Use on a regular cadence (weekly or when the issue list grows unwieldy) to keep the project's open questions coherent, assigned, and at the right level of specificity.
---

# Skill: Issue triage

## When to use
- Weekly coordination review
- After a burst of new issues from a PI or literature review
- When work seems blocked or directionless
- Before a milestone deadline

## Steps

### 1. Review all open issues

For each open issue, check:

| Question | Action if no |
|----------|-------------|
| Is it assigned? | Assign to person or agent |
| Is it scoped to a single answerable question? | Split or rewrite |
| Is it at the right level? (S1 task vs S4 question) | Relabel or elevate |
| Is it blocked? | Add `blocked` label, note what it's waiting on |
| Is it a duplicate? | Close with reference to original |
| Has it been open too long without progress? | Comment asking for status or reassign |

### 2. Check for missing skills
If the same type of issue keeps appearing and no skill covers it,
open a new issue: `Draft skill for <task type>` — label `skill-gap`

### 3. Check for skill-to-software candidates
If any skill has been executed many times without modification,
open an issue: `Graduate <skill> to software` — label `skill-to-software`

### 4. Check milestone health
- Are all milestone issues assigned?
- Is the milestone achievable in the time remaining?
- If not: flag to PI level (S5) — open issue with label `milestone-risk`

### 5. Write a triage summary comment
On the milestone or a designated coordination issue, post:
```
## Triage — YYYY-MM-DD
- Open issues: N
- Newly assigned: N
- Blocked: N (list)
- Skill gaps identified: N (list)
- Milestone risk: yes/no
```

## Output
A cleaner, fully-assigned issue list.
Any structural problems (skill gaps, milestone risk) surfaced as new issues.
No commits required — triage is coordination, not contribution.
