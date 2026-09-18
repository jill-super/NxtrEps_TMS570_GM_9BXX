---
title: "Start-Stop Function (GMStrtStop)"
description: "Implements customer feature CF12A: steering behavior across engine start-stop events."
---

# Start-Stop Function

Directory: `GMStrtStop` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements customer feature CF12A: steering behavior across engine start-stop events.

## Source layout

Repository path: `GMStrtStop/`

| File | Role |
| --- | --- |
| `GMStrtStop/src/Ap_GMStrtStop.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_StrtStop_Per1_SSScale_Uls_f32()`
- `Rte_IWrite_StrtStop_Per1_SSSlew_UlspS_f32()`
- `Rte_IWrite_StrtStop_Per1_SSState_State_enum()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_GMStrtStop.h`
- `SystemTime.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
