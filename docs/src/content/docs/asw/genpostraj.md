---
title: "General Position Trajectory Generation (GenPosTraj)"
description: "Generates smooth position trajectories for scripted/assisted steering motions."
---

# General Position Trajectory Generation

Directory: `GenPosTraj` · AUTOSAR group: Application Software


## Purpose and responsibility

Generates smooth position trajectories for scripted/assisted steering motions.

## Source layout

Repository path: `GenPosTraj/`

| File | Role |
| --- | --- |
| `GenPosTraj/src/Ap_GenPosTraj.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_GenPosTraj_Per1_PosTrajHwAngle_HwDeg_f32()`
- `GenPosTraj_SCom_SetInputParam()`


## Dependencies

- `Ap_GenPosTraj_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_GenPosTraj.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
