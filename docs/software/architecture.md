# Software architecture

Status: DRAFT / planned, nothing implemented yet. ROS 2 usage undecided.

```mermaid
flowchart LR
    FT[KWR75 F/T sensor] --> FTD[F/T driver]
    CAM[ZED Mini] --> CAMD[Camera capture]
    GW[Gripper width (TODO: how measured)] --> REC
    FTD --> REC[Recorder: timestamped data]
    CAMD --> REC
    REC --> DATA[(data/raw)]
    DATA --> PROC[scripts/: processing]
    PROC --> OUT[(data/processed, figures)]
    OUT -.-> ROBOT[Franka FR3 execution (scope TODO)]
```

## Components
TODO: list once decided.
