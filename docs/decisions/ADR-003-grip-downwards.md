# ADR-003: Grip direction downwards instead of forward

- Date: TODO (between 2026-10-04 and 2026-10-07; reconstructed from sketches)
- Status: active

## Context
The original UMI grips forward. The Franka mainly works with the gripper pointing down.

## Options
1. Keep forward grip (original UMI).
2. Grip downwards.

## Decision
Grip downwards. Gripping mechanism functionally the same as the original; finger holders redesigned to point down; trigger longer because it must go around the F/T sensor.

## Rationale
Matches the typical Franka use and the intended robot tasks (insertion, fragile objects).

## Consequences
- Weight now hangs below the hand instead of pressing from above → handle ergonomics changed.
- Finger holders and handle redesigned.
- Camera/TCP/sensor offsets must be recomputed (V3 work, `docs/calibration.md`).
