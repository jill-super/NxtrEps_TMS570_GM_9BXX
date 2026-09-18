---
title: "Handwheel Torque Correlation Diagnostic (HwTqCorrln)"
description: "Implements the \"Hand Wheel Torque Immediate and Long term Correlation diagnostic\" (engineering specification ES-57B)."
---

# Handwheel Torque Correlation Diagnostic

Directory: `HwTqCorrln` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements the "Hand Wheel Torque Immediate and Long term Correlation diagnostic" (engineering specification ES-57B).

## Source layout

Repository path: `HwTqCorrln/`

| File | Role |
| --- | --- |
| `HwTqCorrln/src/Sa_HwTqCorrln.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_HwTqCorrln_Per1_HwTqCorrlnSts_Cnt_u16()`
- `Rte_IWrite_HwTqCorrln_Per2_HwTqIdptSig_Cnt_u08()`
- `Rte_IWrite_HwTqCorrln_Per2_HwTqVldSrcSig_Cnt_u08()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Sa_HwTqCorrln.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
