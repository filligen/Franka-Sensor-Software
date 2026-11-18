# CLAUDE.md – Rules for maintaining the thesis knowledge base

Project: Bachelor thesis "Design and Testing of a UMI-Based Gripper with Integrated Six-Axis Force/Torque Sensor" (pd|z, ETH Zurich). Author: Fynn Illigen. Read `docs/00_project/brief.md` first.

Language: chat with the user in German (unless they switch); **every file in the repo is written in English** (the thesis is in English). Style: short, factual, with numbers and units; no prose padding.

Goal: the thesis can be written almost directly from this repo. Every session keeps it up to date.

## Rules

1. **Journal.** At the end of every session create or extend `docs/journal/YYYY-MM-DD.md`: what was done, what was observed (with numbers), what did not work and why, open questions, next steps.
2. **ADRs.** Record every non-trivial decision as `docs/decisions/ADR-nnn-<title>.md`, including rejected options. Rejected approaches with reasons are valuable for the Discussion.
3. **Runs.** Every run counts, also failed and excluded ones. Log each in the experiment's `runs.csv` with a reason. Exclusion criteria are defined in the experiment README *before* evaluating.
4. **Parameters.** Never change a parameter only in code. Update `docs/parameters.md` (new value, date, reason). For experiments, copy the current state to the experiment's `params.yaml`.
5. **Reproducibility.** Every number that goes into the thesis must be reproducible from a file in `data/` and a script in `scripts/`. The experiment README references script and commit.
6. **Figures.** Generate figures only via scripts. Photos/screenshots go to `figures/` with date and a short description (see `figures/README.md`).
7. **Sources.** Papers, datasheets, prices, web pages: add to `docs/literature/references.bib` immediately (with access date) and create a note in `docs/literature/notes/<key>.md`. Key format `AuthorYear_keyword`.
8. **Issues.** Update `docs/issues.md` as soon as an error occurs repeatedly: name the failure mode, count occurrences.
9. **Thesis map.** Update `docs/thesis_map.md` when something clearly belongs to a chapter.
10. **Commits.** Small, descriptive commits: `type(scope): message` with type in `feat, fix, exp, docs, data, hw, refactor`. Milestones as git tags (`v0.1-first-run`, …) plus an entry in `CHANGELOG.md`. Commit and push to `main` (explicit decision of the author), unless told otherwise.
11. **Never invent.** Missing values are marked `TODO:` and the author is asked. This includes dates, dimensions, prices and measurements.
12. **Wrap up.** When the user says "Session beenden" or "wrap up": update journal, affected docs and `issues.md`, commit, push, and summarize in a few lines.

## Conventions

- IDs: `ADR-nnn`, `EXP-nnn`, `ISS-nnn`; hardware iterations `V1, V2, …` (see `docs/hardware/iterations.md`).
- Dates: ISO `YYYY-MM-DD`. Units: SI, always written next to the value.
- Large files (bags, videos, SVO, raw logs) are never committed; see `data/raw/README.md`. No Git LFS.
- Reconstructed (retroactive) entries are marked `(reconstructed)`; uncertain dates are marked `TODO:` or `~`.
- Templates live in `templates/`. Keep them lean: few mandatory fields.
