---
title: "End-of-Travel Actuator Management (EOTActuatorMng)"
description: "Manages actuator behavior near the mechanical end of travel (rack end stops)."
---

# End-of-Travel Actuator Management

Directory: `EOTActuatorMng` · AUTOSAR group: Application Software


## Purpose and responsibility

Manages actuator behavior near the mechanical end of travel (rack end stops).

## Source layout

Repository path: `EOTActuatorMng/`

| File | Role |
| --- | --- |
| `EOTActuatorMng/src/Ap_EOTActuatorMng.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_EOTActuatorMng_Per1_AssistEOTDamping_MtrNm_f32()`
- `Rte_IWrite_EOTActuatorMng_Per1_AssistEOTGain_Uls_f32()`
- `Rte_IWrite_EOTActuatorMng_Per1_AssistEOTLimit_MtrNm_f32()`


## Dependencies

- `Ap_EOTActuatorMng_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_EOTActuatorMng.h`
- `filters.h`
- `fixmath.h`
- `fpmtype.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
