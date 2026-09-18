---
title: "Steering Damping Control (Damping)"
description: "Provides speed-sensitive steering damping for stability and feel."
---

# Steering Damping Control

Directory: `Damping` · AUTOSAR group: Application Software


## Purpose and responsibility

Provides speed-sensitive steering damping for stability and feel.

## Source layout

Repository path: `Damping/`

| File | Role |
| --- | --- |
| `Damping/src/Ap_Damping.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_Damping_Per1_DampingCmd_MtrNm_f32()`


## Dependencies

- `Ap_Damping_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_Damping.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
