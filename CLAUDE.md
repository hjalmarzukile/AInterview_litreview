# AInterview_litreview — Project OS

This repo is governed by the Research Org OS. Agents operating here run at S1 by default.

## Project
Literature review: AI in qualitative interviews — methods, tools, ethics, current state.

## Roles
- PI: hjalmarzukile
- Student: gaardhus (S1)

## Issue Hierarchy
- **Epic** (label: `epic`) — broad research task, assigned by PI, closes with PI approval
- **Task** (label: `task`) — actionable sub-task, deserves a commit, approval set per issue
- Use `#parent: <issue-number>` in task body to link to parent epic

## Approval Rules
- `pi-approve` label → issue cannot be closed without PI approving via overlay
- `self-approve` label → student/agent can close directly

## Commit Format
```
type(scope): description — closes #N
```
Types: `lit`, `data`, `analysis`, `skill`, `fix`, `admin`

## Privacy
If any task involves personal identifiers or sensitive data → run `manual-required` skill immediately. Do not proceed.

## Skills
See `skills/` directory. Always check for an existing skill before starting a new task type.

## Folder Structure
```
data/raw/          ← unmodified source data
data/processed/    ← cleaned data
literature/summaries/  ← author_year.md structured summaries
literature/pdfs/   ← downloaded PDFs
analysis/scripts/  ← Python scripts
logs/manual/       ← manual-required log files
skills/            ← workflow instructions
```
