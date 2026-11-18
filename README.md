# Franka-Sensor-Software

Bachelor thesis at the Product Development Group Zurich (pd|z), ETH Zurich:
**Design and Testing of a UMI-Based Gripper with Integrated Six-Axis Force/Torque Sensor**

- Author: Fynn Illigen
- Supervisor: Lucas Gimeno | Professor: Prof. Dr. M. Meboldt
- Period: 2026-10-04 → 2027-01-31
- Stack: Franka FR3, Kunwei KWR75 (6-axis F/T), ZED Mini, Fusion 360, Python

This repo is the thesis **knowledge base**: code, decisions, experiments, logs, parameters, failures, literature and meetings. The goal is to write the thesis almost directly from it.

## Setup

TODO: Python version and dependency management (not decided yet).
TODO: ROS 2 yes/no (not decided yet; see `docs/decisions/` once an ADR exists).

## Launch order

TODO: fill in once the first software runs (sensor driver → camera → recorder → robot).

## Folder map

| Path | Content |
|---|---|
| `CLAUDE.md` | Rules for maintaining this knowledge base (read first in every session) |
| `CHANGELOG.md` | Milestones and versions |
| `docs/00_project/` | Brief, timeline (plan vs. actual), glossary |
| `docs/journal/` | One log per working day (`YYYY-MM-DD.md`) |
| `docs/decisions/` | ADRs, incl. rejected options |
| `docs/experiments/` | `EXP-nnn-<title>/` with README, `runs.csv`, `params.yaml` |
| `docs/hardware/` | BOM, design iterations, assembly |
| `docs/software/` | Architecture, interfaces and frames |
| `docs/parameters.md` | Single source of truth for all parameters |
| `docs/calibration.md` | F/T sensor, camera, hand-eye, offsets |
| `docs/issues.md` | Known problems and failure modes |
| `docs/meetings/` | Supervisor meetings |
| `docs/literature/` | Paper notes + `references.bib` |
| `docs/thesis_map.md` | Which note/experiment/figure belongs to which chapter |
| `data/raw/` | Small raw data (large data lives externally, see `data/raw/README.md`) |
| `data/processed/` | Derived data, always reproducible from `scripts/` |
| `scripts/` | Evaluation and plot scripts (one per figure) |
| `figures/` | Generated figures + photos with caption notes |
| `src/` | Code |
| `cad/` | STEP/STL exports per iteration |
| `thesis/` | LaTeX (later) |
| `templates/` | Templates for journal, ADR, experiment, meeting, literature note |
