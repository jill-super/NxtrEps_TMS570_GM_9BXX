---
title: "Assist Limit, Current Mode (AstLmt_CM)"
description: "Assist-limit function in current-mode control form (System Function SF04B family). Assumption: suffix CM expands to Current Mode, consistent with the sibling mo"
---

# Assist Limit, Current Mode

Directory: `AstLmt_CM` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Assist-limit function in current-mode control form (System Function SF04B family). Assumption: suffix CM expands to Current Mode, consistent with the sibling motor-control drivers.

## Source layout

Repository path: `AstLmt_CM/`

| File | Role |
| --- | --- |
| `AstLmt_CM/src/Ap_AstLmt.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_AstLmt_Per1_LimitPercentFiltered_Uls_f32()`
- `Rte_IWrite_AstLmt_Per1_PreLimitForStall_MtrNm_f32()`
- `Rte_IWrite_AstLmt_Per1_PreLimitTorque_MtrNm_f32()`
- `Rte_IWrite_AstLmt_Per1_SumLimTrqCmd_MtrNm_f32()`
- `Rte_IWrite_AstLmt_Per1_TrqLimitMin_MtrNm_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_AstLmt.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
