---
title: "Stability Compensation (StabilityComp)"
description: "Adds stabilizing compensation to the steering control loop."
---

# Stability Compensation

Directory: `StabilityComp` · AUTOSAR group: Application Software


## Purpose and responsibility

Adds stabilizing compensation to the steering control loop.

## Source layout

Repository path: `StabilityComp/`

| File | Role |
| --- | --- |
| `StabilityComp/src/Ap_StabilityComp.c` | Implementation |
| `StabilityComp/src/Ap_StabilityComp2.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_StabilityComp_Per1_AssistCmd_MtrNm_f32()`
- `Rte_IWrite_StabilityComp2_Per1_SysAssistCmd_MtrNm_f32()`


## Dependencies

- `Ap_StabilityComp2_Cfg.h`
- `Ap_StabilityComp_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_StabilityComp.h`
- `Rte_Ap_StabilityComp2.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
