---
title: "Motor Angle Correlation Diagnostic (MotAgCorrln)"
description: "Cross-checks available motor angle signals against each other (functional description ES-55B)."
---

# Motor Angle Correlation Diagnostic

Directory: `MotAgCorrln` · AUTOSAR group: Application Software


## Purpose and responsibility

Cross-checks available motor angle signals against each other (functional description ES-55B).

## Source layout

Repository path: `MotAgCorrln/`

| File | Role |
| --- | --- |
| `MotAgCorrln/src/Ap_MotAgCorrln.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_MotAgCorrln_Per1_MtrPosCorrlnSts_Cnt_u16()`
- `Rte_IWrite_MotAgCorrln_Per1_MtrPosIdptSig_Cnt_u08()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_MotAgCorrln.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
