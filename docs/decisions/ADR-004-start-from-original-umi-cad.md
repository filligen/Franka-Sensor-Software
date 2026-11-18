# ADR-004: Start from the original UMI CAD and remove unneeded parts

- Date: 2026-10-07
- Status: active

## Context
Original UMI CAD files are available.

## Options
1. Design from scratch.
2. Adopt original CAD, remove what is not needed, modify the rest.

## Decision
Option 2. Removed: GoPro holder, side mirrors for implicit stereo, rear box.

## Rationale
- The mechanism (linkages, gears, sled) is proven; saves design time.
- Side mirrors are unnecessary because all available cameras are already stereo (ZED Mini).

## Consequences
- Part tolerances of the original were not carried over reliably to our printer/material (ISS-007).
- Camera mount has to be designed anew.
