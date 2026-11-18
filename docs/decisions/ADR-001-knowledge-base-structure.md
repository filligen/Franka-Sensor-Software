# ADR-001: Repository as full knowledge base

- Date: 2026-11-18
- Status: active

## Context
The thesis (2026-10-04 → 2027-01-31) involves hardware iterations, experiments, parameter tuning and many small decisions. Writing the thesis from memory is error-prone.

## Options
1. Code-only repo, notes elsewhere (Notion, paper notebook).
2. Repo as knowledge base: decisions, experiments, logs, parameters, literature, meetings next to the code.

## Decision
Option 2, with the structure described in `README.md` and the rules in `CLAUDE.md`. No Git LFS; large raw data lives outside the repo (`data/raw/README.md`).

## Rationale
- Everything versioned and linked to commits.
- Thesis map (`docs/thesis_map.md`) lets chapters be written from notes.
- Lean templates keep the effort low.

## Consequences
- Every session ends with journal/doc updates (`CLAUDE.md` rule 1, 12).
- Past work (before 2026-11-18) is reconstructed from the author's account and marked `(reconstructed)`.
