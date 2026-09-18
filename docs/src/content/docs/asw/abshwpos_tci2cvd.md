---
title: "Absolute Hardware Position over Inter-Integrated Circuit (AbsHwPos_TcI2cVd)"
description: "Absolute handwheel/column position acquisition path that uses the trusted Inter-Integrated Circuit sensor channel. Implemented as AUTOSAR Software Component Ap_"
---

# Absolute Hardware Position over Inter-Integrated Circuit

Directory: `AbsHwPos_TcI2cVd` · AUTOSAR group: Application Software


## Purpose and responsibility

Absolute handwheel/column position acquisition path that uses the trusted Inter-Integrated Circuit sensor channel. Implemented as AUTOSAR Software Component Ap_AbsHwPos.

## Source layout

Repository path: `AbsHwPos_TcI2cVd/`

| File | Role |
| --- | --- |
| `AbsHwPos_TcI2cVd/src/Ap_AbsHwPos.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_AbsHwPos_Init1_HwPosSource_Cnt_u16()`
- `Rte_IWrite_AbsHwPos_Init1_SrlComHwPosStatus_Cnt_u16()`
- `Rte_IWrite_AbsHwPos_Per1_RelHwPos_HwDeg_f32()`
- `Rte_IWrite_AbsHwPos_Per2_HandwheelAuthority_Uls_f32()`
- `Rte_IWrite_AbsHwPos_Per2_HandwheelPosition_HwDeg_f32()`
- `Rte_IWrite_AbsHwPos_Per2_HwPosSource_Cnt_u16()`
- `Rte_IWrite_AbsHwPos_Per2_SrlComHwPosStatus_Cnt_u16()`
- `Rte_IWrite_AbsHwPos_Per2_SrlComHwPos_HwDeg_f32()`
- `AbsHwPos_SCom_CustClrTrim()`
- `AbsHwPos_SCom_NxtClearTrim()`


## Dependencies

- `Ap_AbsHwPos_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_AbsHwPos.h`
- `filters.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
