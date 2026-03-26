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
| `lit` | literature summaries or reviews |
| `skill` | skill file additions or updates |
| `code` | software in `src/` |
| `fix` | corrections to prior commits |
| `infra` | repo config, CI, tooling |
| `log` | manual-required log entries |

### Examples
```
data(wave3): add preprocessed survey responses — closes #14
analysis(regression): run baseline model on cohort A — closes #17
lit(pearl2009): summarise DAG framework — closes #5
paper(intro): revise framing per reviewer 2 — closes #31
skill(lit-review): add systematic review workflow — closes #8
log: manual required — anonymise participant records #22
```

## Checklist before committing

- [ ] Work resolves a specific issue or todo — issue number known
- [ ] No personal or sensitive data in the commit
- [ ] Files are in the correct directory (`data/`, `analysis/`, `paper/`, `literature/`, etc.)
- [ ] Commit message follows the format above
- [ ] If changing a skill: PR opened, not committed directly to main

## Personal data check
If any file in the commit contains personal identifiers (names, IDs,
contact info, health records) — **stop**.
Follow the `manual-required` skill instead.

---

## After committing: post a PI summary

After every commit, post a short summary as a commit comment on GitHub.
This is how the PI tracks what is happening without reading diffs.

### Step 1 — draft the summary
Read the diff (`git diff HEAD~1..HEAD`) and the commit message.
Draft a summary of **2–3 sentences** that answers:
- What was done
- What it contributes to the research question
- Anything the PI should know or decide

Write it plainly. No jargon. Assume the PI has not seen the files.

### Step 2 — show the student for approval
Present the draft to the student:
> "Here is the summary I'll post to GitHub for the PI. Edit or approve:"
> [draft text]

Wait for the student to confirm or edit. Do not post without approval.

### Step 3 — post as a commit comment
Once approved, post using the GitHub API:

```bash
curl -s -X POST \
  -H "Authorization: token $GITHUB_TOKEN" \
  -H "Content-Type: application/json" \
  https://api.github.com/repos/OWNER/REPO/commits/COMMIT_SHA/comments \
  -d '{
    "body": "<!-- commit-summary -->\n**Summary:** APPROVED_TEXT"
  }'
```

Replace:
- `$GITHUB_TOKEN` — use the token in your local environment or `access.md`
- `OWNER/REPO` — the project repo (e.g. `hjalmarzukile/AInterview_litreview`)
- `COMMIT_SHA` — from `git rev-parse HEAD`
- `APPROVED_TEXT` — the student-approved summary

### What good summaries look like

> Added structured summary of Pearl (2009) on causal DAGs. Covers core notation, do-calculus, and backdoor criterion. Relevant to RQ2 on identifying causal pathways in AI-interview data — no PI decision needed.

> Cleaned raw interview transcripts: removed duplicate rows, standardised timestamp format, saved to data/processed/. 847 rows retained from 901 original. Three rows flagged as duplicates are logged in data/codebooks/cleaning_notes.md.

> PI note: the coding scheme in analysis/scripts/code_themes.py needs your input on whether "AI transparency" belongs under theme 3 or theme 4 — see issue #8.
