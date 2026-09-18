---
title: "Active Pull Compensation (ActivePull)"
description: "Compensates vehicle pull/drift by adding a corrective assist offset (System Function SF013A family)."
---

# Active Pull Compensation

Directory: `ActivePull` · AUTOSAR group: Application Software


## Purpose and responsibility

Compensates vehicle pull/drift by adding a corrective assist offset (System Function SF013A family).

## Source layout

Repository path: `ActivePull/`

| File | Role |
| --- | --- |
| `ActivePull/src/Ap_ActivePull.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_ActivePull_Per1_PullCmpShoTermIntgtrSt_HwNm_f32()`
- `Rte_IWrite_ActivePull_Per2_PullCompCmd_MtrNm_f32()`
- `Rte_IWrite_ActivePull_Per3_PullCmpLongTermIntgtrSt_HwNm_f32()`
- `ActivePull_SCom_ReadParam()`
- `ActivePull_SCom_Reset()`
- `ActivePull_SCom_SetLTComp()`
- `ActivePull_SCom_SetSTComp()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_ActivePull.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
