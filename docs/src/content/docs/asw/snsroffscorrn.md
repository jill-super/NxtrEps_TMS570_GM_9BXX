---
title: "Sensor Offset Correction (SnsrOffsCorrn)"
description: "Corrects offsets of yaw rate, handwheel position, and handwheel torque signals."
---

# Sensor Offset Correction

Directory: `SnsrOffsCorrn` · AUTOSAR group: Application Software


## Purpose and responsibility

Corrects offsets of yaw rate, handwheel position, and handwheel torque signals.

## Source layout

Repository path: `SnsrOffsCorrn/`

| File | Role |
| --- | --- |
| `SnsrOffsCorrn/src/Ap_SnsrOffsCorrn.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_SnsrOffsCorrn_Per1_HwAgCorrd_HwDeg_f32()`
- `Rte_IWrite_SnsrOffsCorrn_Per1_HwTqCorrd_HwNm_f32()`
- `Rte_IWrite_SnsrOffsCorrn_Per1_YawRateCorrd_DegpS_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_SnsrOffsCorrn.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
