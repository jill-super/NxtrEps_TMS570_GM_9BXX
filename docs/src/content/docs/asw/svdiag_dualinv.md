---
title: "Sine Voltage Generation Diagnostics, Dual Inverter (SVDiag_DualInv)"
description: "Sine voltage generation diagnostics for the dual-inverter power stage: phase-reasonableness checks and motor-drive diagnostics."
---

# Sine Voltage Generation Diagnostics, Dual Inverter

Directory: `SVDiag_DualInv` · AUTOSAR group: Application Software


## Purpose and responsibility

Sine voltage generation diagnostics for the dual-inverter power stage: phase-reasonableness checks and motor-drive diagnostics.

## Source layout

Repository path: `SVDiag_DualInv/`

| File | Role |
| --- | --- |
| `SVDiag_DualInv/src/Ap_DigPhsReasDiag.c` | Implementation |
| `SVDiag_DualInv/src/Sa_MtrDrvDiag.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_MtrDrvDiag_Per1_GateDrive1ResetActive_Cnt_lgc()`
- `Rte_IWrite_MtrDrvDiag_Per1_GateDrive2ResetActive_Cnt_lgc()`
- `Rte_IWrite_MtrDrvDiag_Per1_MtrDrvr1InitComplete_Cnt_lgc()`
- `Rte_IWrite_MtrDrvDiag_Per1_MtrDrvr2InitComplete_Cnt_lgc()`
- `Rte_IWrite_MtrDrvDiag_Trns1_MtrDrvr1InitComplete_Cnt_lgc()`
- `Rte_IWrite_MtrDrvDiag_Trns1_MtrDrvr2InitComplete_Cnt_lgc()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Os.h`
- `Rte_Ap_DigPhsReasDiag.h`
- `Rte_Sa_MtrDrvDiag.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
