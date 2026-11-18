# ADR-007: Adapt the Franka Hand fingers to the handheld gripper fingers

- Date: 2026-11-18
- Status: active

## Context
For imitation learning, the geometry between TCP and F/T sensor should be identical on the handheld gripper (demonstration) and on the Franka Hand (execution). The finger length and the sensor-to-TCP distance must therefore be matched on both systems.

## Options
1. **Adapt the handheld gripper fingers** to the existing Franka Hand / F/T sensor geometry.
   - Pros: No new end-effector (EE) transform for the Franka Hand; one part fewer to design; the Franka Hand with its original fingers is proven, new fingers could introduce problems.
   - Cons: The handheld gripper fingers are much longer than the Franka fingers. A solution is needed to fit them between TCP and F/T sensor when both systems grip from top to bottom.
2. **Adapt the Franka Hand fingers** to the handheld gripper fingers (new custom fingers on the Franka Hand).
   - Pros: Both systems use (nearly) identical fingers, so the camera perspective is more similar.
   - Cons: The camera mount may obstruct the view. New finger parts must be designed and validated; the Franka Hand needs a new EE transform (TODO: confirm).

## Decision
Option 2: design Franka Hand fingers that match the handheld gripper fingers.

## Rationale
The camera sees the fingers in every frame. With identical fingers, the demonstration and execution views are visually similar. With option 1, the gripper camera would see the gripper fingers during demonstrations and the Franka camera the Franka fingers during execution. The working hypothesis is that this visual domain gap would degrade imitation learning noticeably. Imitation learning performance is the central goal of the thesis, so visual consistency was prioritised over design effort and the proven original fingers. (Hypothesis, not yet tested.)

## Consequences
TODO: to be determined (e.g. finger design, EE transform, validation of the new fingers).
Known open risk: camera mount may obstruct the view (see Cons of option 2).
