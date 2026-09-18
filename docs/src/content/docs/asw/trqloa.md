---
title: "Torque Path Loss-of-Assist Handling (TrqLOA)"
description: "Torque-path behavior under loss-of-assist conditions."
---

# Torque Path Loss-of-Assist Handling

Directory: `TrqLOA` · AUTOSAR group: Application Software


## Purpose and responsibility

Torque-path behavior under loss-of-assist conditions.

## Source layout

Repository path: `TrqLOA/`

| File | Role |
| --- | --- |
| `TrqLOA/src/Ap_TrqLOA.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_TrqLOA_Per1_TrqLOAAvail_Cnt_lgc()`
- `Rte_IWrite_TrqLOA_Per1_TrqLOACmd_MtrNm_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_TrqLOA.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
