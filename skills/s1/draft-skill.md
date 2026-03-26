---
name: draft-skill
level: s1
description: Use after completing a novel task well, or when a recurring task lacks a standard approach. Creates a draft skill for review.
---

# Skill: Draft a new skill

## When to use
- You just completed a task that took significant judgment
- The same task will likely recur
- No existing skill covered it adequately
- A researcher asks for a workflow to be standardised

## Steps

### 1. Determine the skill level
| Level | For tasks that involve |
|-------|----------------------|
| `s1` | execution, specific analysis, committing artifacts |
| `s3` | coordination, triage, cross-project decisions |
| `s4` | synthesis, literature, methodology, field scanning |

### 2. Create the draft file
Path: `skills/drafts/<skill-name>.md`

### 3. Use this structure

```markdown
---
name: skill-name
level: s1 | s3 | s4
description: One sentence. Start with "Use when..." — this is how the agent selects the skill.
---

# Skill: <Human readable name>

## When to use
<2-3 sentences on the trigger condition>

## Steps
<numbered, concrete, actionable>

## Checks / gotchas
<what commonly goes wrong>

## Output
<what a good completion looks like — what gets committed>
```

### 4. Open a PR
- Branch: `skill/<skill-name>`
- PR title: `skill: add <skill-name> workflow`
- Request review from the relevant level (S3 reviews S1 skills, S4 reviews S3/S4 skills)

### 5. After merge
Move from `skills/drafts/` to `skills/s1/`, `skills/s3/`, or `skills/s4/`

## Note on skill graduation
When a skill has been used many times without modification and runs at
volume, consider graduating it to deterministic software in `src/`.
Open an issue with label `skill-to-software` to track this.
