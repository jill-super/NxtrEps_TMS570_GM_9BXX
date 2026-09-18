---
title: "Battery Voltage Correlation Diagnostic (BattVltgCorrln)"
description: "Cross-checks redundant battery voltage signals against each other to detect sensor or wiring faults."
---

# Battery Voltage Correlation Diagnostic

Directory: `BattVltgCorrln` · AUTOSAR group: Application Software


## Purpose and responsibility

Cross-checks redundant battery voltage signals against each other to detect sensor or wiring faults.

## Source layout

Repository path: `BattVltgCorrln/`

| File | Role |
| --- | --- |
| `BattVltgCorrln/src/Ap_BattVltgCorrln.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_BattVltgCorrln_Per1_BattSwdVltgCorrlnSts_Cnt_u08()`
- `Rte_IWrite_BattVltgCorrln_Per1_BattVltgCorrlnIdptSig_Cnt_u08()`
- `Rte_IWrite_BattVltgCorrln_Per1_DftBrdgVltgActv_Cnt_lgc()`
- `Rte_IWrite_BattVltgCorrln_Per1_SwdVltgLimd_Cnt_lgc()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_BattVltgCorrln.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
