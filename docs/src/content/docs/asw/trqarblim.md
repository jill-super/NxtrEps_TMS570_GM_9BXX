---
title: "Torque Arbitration Limit, Customer Feature 10 (TrqArblim)"
description: "Implements customer feature CF10: limits on arbitrated torque."
---

# Torque Arbitration Limit, Customer Feature 10

Directory: `TrqArblim` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements customer feature CF10: limits on arbitrated torque.

## Source layout

Repository path: `TrqArblim/`

| File | Role |
| --- | --- |
| `TrqArblim/src/Ap_TrqArblim.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_TrqArblim_Per1_AssistDDFactor_Uls_f32()`
- `Rte_IWrite_TrqArblim_Per1_DampingDDFactor_Uls_f32()`
- `Rte_IWrite_TrqArblim_Per1_ESCIsLimited_Cnt_lgc()`
- `Rte_IWrite_TrqArblim_Per1_ESCTorqueDelivered_HwNm_f32()`
- `Rte_IWrite_TrqArblim_Per1_IqTrqOv_HwNm_f32()`
- `Rte_IWrite_TrqArblim_Per1_LKATorqueDelivered_HwNm_f32()`
- `Rte_IWrite_TrqArblim_Per1_OpTrqOv_MtrNm_f32()`
- `Rte_IWrite_TrqArblim_Per1_PullCmpCustLrngDi_Cnt_lgc()`
- `Rte_IWrite_TrqArblim_Per1_ReturnDDFactor_Uls_f32()`


## Dependencies

- `Ap_TrqArblim_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `Interpolation.h`
- `MemMap.h`
- `Rte_Ap_TrqArblim.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
