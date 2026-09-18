---
title: "State Output Control (StOpCtrl)"
description: "Implements System Function SF05: governs state-dependent outputs of the steering controller."
---

# State Output Control

Directory: `StOpCtrl` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements System Function SF05: governs state-dependent outputs of the steering controller.

## Source layout

Repository path: `StOpCtrl/`

| File | Role |
| --- | --- |
| `StOpCtrl/src/Ap_StOpCtrl.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_StOpCtrl_Per1_OutputRampMult_Uls_f32()`
- `Rte_IWrite_StOpCtrl_Per1_SysStReqDi_Cnt_lgc()`


## Dependencies

- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_StOpCtrl.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
