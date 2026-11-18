# Project brief

## Title
Design and Testing of a UMI-Based Gripper with Integrated Six-Axis Force/Torque Sensor

## Organisation
- Product Development Group Zurich (pd|z), ETH Zurich
- Author: Fynn Illigen (5th-semester BSc mechanical engineering → TODO: confirm formal programme/degree wording)
- Supervisor: Lucas Gimeno
- Professor: Prof. Dr. M. Meboldt
- Start: 2026-10-04 | Submission: 2027-01-31
- Language of the thesis: English

## Task description
The Universal Manipulation Interface (UMI) enables the collection of robot demonstrations with a handheld, camera-equipped gripper, but it relies on visual information and gripper width only and provides no force information. This thesis develops a UMI-based gripper with an integrated six-axis force/torque sensor, so that interaction forces can be recorded during demonstrations. The gripper is designed for use on a Franka robot, where the recorded forces can be used during execution of contact-rich tasks such as part insertion or handling fragile objects.

## Stack
Franka FR3, Kunwei KWR75 (six-axis F/T sensor), ZED Mini, Fusion 360, Python. ROS 2: TODO (undecided).

## Goals
1. Mechanical design of a UMI-based handheld gripper with an integrated F/T sensor (sensor between handle and gripping mechanism).
2. Gripper usable on the Franka FR3 (grasping downwards, matching the typical Franka workspace use).
3. Record interaction forces synchronously with vision and gripper width during demonstrations. TODO: confirm.
4. TODO: Use of recorded forces during robot execution (scope level to be agreed with supervisor).

## Scope / out of scope
- In scope: TODO
- Out of scope: TODO (e.g. policy learning pipeline changes?)

## Success criteria
TODO: define measurable criteria with supervisor (e.g. force range/resolution, usability, successful demo tasks).

## Related work
Chi et al., UMI (see `docs/literature/`).
