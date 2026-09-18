---
title: "Power Limit Function Correction (PwrLmtFuncCr)"
description: "Corrects/coordinates the power-limit function with thermal and voltage derating."
---

# Power Limit Function Correction

Directory: `PwrLmtFuncCr` · AUTOSAR group: Application Software


## Purpose and responsibility

Corrects/coordinates the power-limit function with thermal and voltage derating.

## Source layout

Repository path: `PwrLmtFuncCr/`

| File | Role |
| --- | --- |
| `PwrLmtFuncCr/src/Ap_PwrLmtFuncCr.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_PwrLmtFuncCr_Per1_MRFMtrTrqCmd_MtrNm_f32()`
- `Rte_IWrite_PwrLmtFuncCr_Per2_FltTrqLmt_Uls_f32()`
- `Rte_IWrite_PwrLmtFuncCr_Per2_ThresholdExceeded_Cnt_lgc()`


## Dependencies

- `Ap_DiagMgr.h`
- `Ap_PwrLmtFuncCr_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_PwrLmtFuncCr.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
