---
name: literature-review
level: s4
description: Use when scoping a new research question, preparing a paper section, or mapping a field. Produces a structured synthesis committed to the knowledge base.
---

# Skill: Literature review

## When to use
- A new research question needs grounding in existing work
- A paper section requires a state-of-the-art summary
- A methodology choice needs comparative justification

## Steps

### 1. Open an issue first
Title format: `Literature review: <topic or question>`
Label: `task`

### 2. Define the scope in the issue
Before searching, write in the issue:
- The specific question the review should answer
- Date range (e.g. 2018–present)
- Key databases to search (e.g. Scopus, PubMed, Google Scholar, arXiv)
- Inclusion/exclusion criteria
- Expected output format (summary table, narrative, annotated bib)

### 3. Search and collect
- Run searches with documented query strings
- Record query strings in the issue or a `data/lit/queries.md` file
- Collect results into `data/lit/raw/` as BibTeX or CSV exports

⚠️ If any source requires institutional login or personal credentials
— flag in issue, mark `manual-required`, human downloads locally.

### 4. Screen and filter
- Remove duplicates
- Apply inclusion/exclusion criteria
- Record excluded items with reason in `data/lit/excluded.md`

### 5. Synthesise
Produce one of:
- `analysis/lit/<topic>-summary.md` — narrative synthesis
- `analysis/lit/<topic>-table.md` — structured comparison table
- `analysis/lit/<topic>-annotated.bib` — annotated bibliography

### 6. Commit
```
analysis(lit): synthesise <topic> literature — closes #N
```

## Quality checks
- Every claim in the synthesis traceable to a citation
- Gaps and contradictions noted explicitly — these become new issues
- Summary states what the review does NOT cover

## Output of a good literature review
A document that answers the scoping question, notes open gaps,
and generates 2–5 new issues for unresolved questions.
