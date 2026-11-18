# ADR-002: Mechanical (not electronic) trigger actuation

- Date: ~2026-10-06 (reconstructed, TODO: confirm exact date)
- Status: active

## Context
The F/T sensor must sit between the handle and the gripping mechanism so that all handle forces pass through it. The mechanism must therefore be actuated across the sensor.

## Options
1. Electronic actuation (button/motor).
2. Mechanical trigger that reaches around the sensor.

## Decision
Mechanical trigger; the trigger is routed around the F/T sensor.

## Rationale
Electronic actuation was judged as very complicated. With the mechanical solution only the trigger geometry around the sensor has to be designed; the original UMI mechanism stays functionally unchanged.

## Consequences
- Trigger is much longer than in the original UMI because it wraps around the sensor (hook).
- Long, thin sections are prone to bending/breaking (ISS-008).
- Trigger hook geometry became a recurring design topic (ADR-006).
