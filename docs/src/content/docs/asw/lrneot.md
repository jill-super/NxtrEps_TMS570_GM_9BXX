---
title: "End-of-Travel Learning (LrnEOT)"
description: "Learns the mechanical end-of-travel positions during operation or service routines."
---

# End-of-Travel Learning

Directory: `LrnEOT` · AUTOSAR group: Application Software


## Purpose and responsibility

Learns the mechanical end-of-travel positions during operation or service routines.

## Source layout

Repository path: `LrnEOT/`

| File | Role |
| --- | --- |
| `LrnEOT/src/Ap_LrnEOT.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_LrnEOT_Init1_CCWFound_Cnt_lgc()`
- `Rte_IWrite_LrnEOT_Init1_CCWPosition_HwDeg_f32()`
- `Rte_IWrite_LrnEOT_Init1_CWFound_Cnt_lgc()`
- `Rte_IWrite_LrnEOT_Init1_CWPosition_HwDeg_f32()`
- `Rte_IWrite_LrnEOT_Per1_CCWFound_Cnt_lgc()`
- `Rte_IWrite_LrnEOT_Per1_CCWPosition_HwDeg_f32()`
- `Rte_IWrite_LrnEOT_Per1_CWFound_Cnt_lgc()`
- `Rte_IWrite_LrnEOT_Per1_CWPosition_HwDeg_f32()`
- `LrnEOT_Scom_ResetEOT()`


## Dependencies

- `Ap_LrnEOT_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_LrnEOT.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
