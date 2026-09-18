---
title: "Hands-Off-Wheel Detection (HOWDetect)"
description: "Detects hands-off-wheel condition from torque/activity signatures for driver-assistance interaction."
---

# Hands-Off-Wheel Detection

Directory: `HOWDetect` · AUTOSAR group: Application Software


## Purpose and responsibility

Detects hands-off-wheel condition from torque/activity signatures for driver-assistance interaction.

## Source layout

Repository path: `HOWDetect/`

| File | Role |
| --- | --- |
| `HOWDetect/src/Ap_HOWDetect.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_HOWDetect_Per1_HOWEstimate_Uls_f32()`
- `Rte_IWrite_HOWDetect_Per1_HOWState_Cnt_s08()`


## Dependencies

- `Ap_HOWDetect_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_HOWDetect.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
