---
title: "Translational Damping, legacy System Function 26 (TranlDampg)"
description: "Damping function for translational/rack dynamics (functional description FDD V001, legacy of System Function SF26)."
---

# Translational Damping, legacy System Function 26

Directory: `TranlDampg` · AUTOSAR group: Application Software


## Purpose and responsibility

Damping function for translational/rack dynamics (functional description FDD V001, legacy of System Function SF26).

## Source layout

Repository path: `TranlDampg/`

| File | Role |
| --- | --- |
| `TranlDampg/src/Ap_TranlDampg.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_Ap_TranlDampg_Per1_CRFMtrTrqCmd_MtrNm_f32()`
- `Rte_IWrite_Ap_TranlDampg_Per1_CntrlDampComp_Cnt_lgc()`
- `Rte_IWrite_Ap_TranlDampg_Per1_MRFMtrTrqCmd_MtrNm_f32()`
- `Rte_IWrite_Ap_TranlDampg_Per1_SysC_CRFMtrTrqCmd_MtrNm_f32()`
- `Rte_IWrite_Ap_TranlDampg_Per1_SysC_MRFMtrTrqCmd_MtrNm_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_TranlDampg.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
