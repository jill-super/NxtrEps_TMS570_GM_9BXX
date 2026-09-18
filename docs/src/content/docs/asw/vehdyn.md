---
title: "Vehicle Dynamics Compensation (VehDyn)"
description: "Implements System Function SF42: compensates steering for vehicle-dynamics states."
---

# Vehicle Dynamics Compensation

Directory: `VehDyn` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements System Function SF42: compensates steering for vehicle-dynamics states.

## Source layout

Repository path: `VehDyn/`

| File | Role |
| --- | --- |
| `VehDyn/src/Ap_VehDyn.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_VehDyn_Per1_SensorlessAuthority_Uls_f32()`
- `Rte_IWrite_VehDyn_Per1_SensorlessHwPos_HwDeg_f32()`
- `VehDyn_SCom_ForceCenter()`
- `VehDyn_SCom_ResetCenter()`


## Dependencies

- `Ap_VehDyn_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_VehDyn.h`
- `SystemTime.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
