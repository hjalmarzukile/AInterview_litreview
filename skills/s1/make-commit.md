---
name: make-commit
level: s1
description: Use when contributing any artifact — code, data, analysis, paper draft, slides, or skill update. Every commit must resolve an issue or named todo.
---

# Skill: Make a commit

## When to use
When work is complete enough to be a meaningful contribution to the knowledge base.
Not for saves or checkpoints — for genuine additions.

## Commit message format

```
type(scope): description — closes #N
```

### Types
| type | use for |
|------|---------|
| `data` | raw or processed dataset changes |
| `analysis` | notebooks, scripts, results |
| `paper` | manuscript draft changes |
| `slides` | presentation changes |
| `skill` | skill file additions or updates |
| `code` | software in `src/` |
| `fix` | corrections to prior commits |
| `infra` | repo config, CI, tooling |
| `log` | manual-required log entries |

### Examples
```
data(wave3): add preprocessed survey responses — closes #14
analysis(regression): run baseline model on cohort A — closes #17
paper(intro): revise framing per reviewer 2 — closes #31
skill(lit-review): add systematic review workflow — closes #8
log: manual required — anonymise participant records #22
```

## Checklist before committing

- [ ] Work resolves a specific issue or todo — issue number known
- [ ] No personal or sensitive data in the commit
- [ ] Files are in the correct directory (`data/`, `analysis/`, `paper/`, etc.)
- [ ] Commit message follows the format above
- [ ] If changing a skill: PR opened, not committed directly to main

## Personal data check
If any file in the commit contains personal identifiers (names, IDs,
contact info, health records) — **stop**.
Follow the `manual-required` skill instead.
