---
title: "Analog Handwheel Torque Sensing (AnaHwTrq)"
description: "Implements the \"Analog Hand Wheel Torque\" subfunction of engineering specification ES-04E: acquisition and conditioning of the analog handwheel torque sensor si"
---

# Analog Handwheel Torque Sensing

Directory: `AnaHwTrq` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements the "Analog Hand Wheel Torque" subfunction of engineering specification ES-04E: acquisition and conditioning of the analog handwheel torque sensor signal.

## Source layout

Repository path: `AnaHwTrq/`

| File | Role |
| --- | --- |
| `AnaHwTrq/src/Sa_AnaHwTrq.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_AnaHwTrq_Init_HwTq1Qlfr_State_enum()`
- `Rte_IWrite_AnaHwTrq_Init_HwTq1RollgCntr_Cnt_u08()`
- `Rte_IWrite_AnaHwTrq_Init_HwTq2Qlfr_State_enum()`
- `Rte_IWrite_AnaHwTrq_Init_HwTq2RollgCntr_Cnt_u08()`
- `Rte_IWrite_AnaHwTrq_Per1_HwTq1Qlfr_State_enum()`
- `Rte_IWrite_AnaHwTrq_Per1_HwTq1RollgCntr_Cnt_u08()`
- `Rte_IWrite_AnaHwTrq_Per1_HwTq1Val_HwNm_f32()`
- `Rte_IWrite_AnaHwTrq_Per2_HwTq2Qlfr_State_enum()`
- `Rte_IWrite_AnaHwTrq_Per2_HwTq2RollgCntr_Cnt_u08()`
- `Rte_IWrite_AnaHwTrq_Per2_HwTq2Val_HwNm_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Sa_AnaHwTrq.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
