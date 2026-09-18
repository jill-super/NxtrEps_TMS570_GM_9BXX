---
title: "Limit Coding (LmtCod)"
description: "Encodes/limits assistance authority (System Function SF38A family)."
---

# Limit Coding

Directory: `LmtCod` · AUTOSAR group: Application Software


## Purpose and responsibility

Encodes/limits assistance authority (System Function SF38A family).

## Source layout

Repository path: `LmtCod/`

| File | Role |
| --- | --- |
| `LmtCod/src/Ap_LmtCod.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_LmtCod_Per1_EOTGainLtd_Uls_f32()`
- `Rte_IWrite_LmtCod_Per1_EOTLimitLtd_MtrNm_f32()`
- `Rte_IWrite_LmtCod_Per1_OutputRampMultLtd_Uls_f32()`
- `Rte_IWrite_LmtCod_Per1_StallLimitLtd_MtrNm_f32()`
- `Rte_IWrite_LmtCod_Per1_ThermalLimitLtd_MtrNm_f32()`
- `Rte_IWrite_LmtCod_Per1_VehSpdLimitLtd_MtrNm_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `Interpolation.h`
- `MemMap.h`
- `Rte_Ap_LmtCod.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
