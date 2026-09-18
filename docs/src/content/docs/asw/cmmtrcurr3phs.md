---
title: "Common Motor Current Measurement, Three-Phase Shunt (CmMtrCurr3Phs)"
description: "Three-phase shunt current measurement for brushless current-mode control (engineering specification ES-01F)."
---

# Common Motor Current Measurement, Three-Phase Shunt

Directory: `CmMtrCurr3Phs` · AUTOSAR group: Application Software


## Purpose and responsibility

Three-phase shunt current measurement for brushless current-mode control (engineering specification ES-01F).

## Source layout

Repository path: `CmMtrCurr3Phs/`

| File | Role |
| --- | --- |
| `CmMtrCurr3Phs/src/Sa_CmMtrCurr3Phs.c` | Implementation |
| `CmMtrCurr3Phs/include/Sa_CmMtrCurr3Phs.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Cm3PhsMtrCurrTempOffset_Scom_Get()`
- `Cm3PhsMtrCurrTempOffset_Scom_Set()`
- `Rte_IWrite_CmMtrCurr3Phs_Per1_MtrCurrATempOffset_Volt_f32()`
- `Rte_IWrite_CmMtrCurr3Phs_Per1_MtrCurrBTempOffset_Volt_f32()`
- `Rte_IWrite_CmMtrCurr3Phs_Per1_MtrCurrCTempOffset_Volt_f32()`
- `Rte_IWrite_CmMtrCurr3Phs_Per2_MtrCurrIdptSig_Cnt_u08()`
- `Rte_IWrite_CmMtrCurr3Phs_Per3_ComOffset_Cnt_u16()`
- `CmMtrCurr3Phs_SCom_Read3PhsMtrCurrCals()`
- `CmMtrCurr3Phs_SCom_Set3PhsMtrCurrCals()`
- `CmMtrCurr_SCom_MtrCurrOffReadStatus()`


## Dependencies

- `CalConstants.h`
- `CmMtrCurr3Phs_Cfg.h`
- `GlobalMacro.h`
- `Interpolation.h`
- `MemMap.h`
- `Rte_Sa_CmMtrCurr3Phs.h`
- `Sa_CmMtrCurr3Phs.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
