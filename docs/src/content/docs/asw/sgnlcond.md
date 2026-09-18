---
title: "Signal Conditioning (SgnlCond)"
description: "Central signal conditioning stage (filtering, scaling, qualification) for application inputs (Software Component Ap_SignlCondn)."
---

# Signal Conditioning

Directory: `SgnlCond` · AUTOSAR group: Application Software


## Purpose and responsibility

Central signal conditioning stage (filtering, scaling, qualification) for application inputs (Software Component Ap_SignlCondn).

## Source layout

Repository path: `SgnlCond/`

| File | Role |
| --- | --- |
| `SgnlCond/src/Ap_SignlCondn.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_SignlCondn_Per1_EstimdLatAcceValid_Cnt_lgc()`
- `Rte_IWrite_SignlCondn_Per1_EstimdLatAcce_MpSecSq_f32()`
- `Rte_IWrite_SignlCondn_Per1_VehicleLatAcceValid_Cnt_lgc()`
- `Rte_IWrite_SignlCondn_Per1_VehicleLatAccel_MpSecSq_f32()`
- `Rte_IWrite_SignlCondn_Per1_VehicleLonAccelValid_Cnt_lgc()`
- `Rte_IWrite_SignlCondn_Per1_VehicleLonAccel_KphpS_f32()`
- `Rte_IWrite_SignlCondn_Per1_VehicleSpeedValid_Cnt_lgc()`
- `Rte_IWrite_SignlCondn_Per1_VehicleSpeed_Kph_f32()`
- `Rte_IWrite_SignlCondn_Per1_VehicleYawRateValid_Cnt_lgc()`
- `Rte_IWrite_SignlCondn_Per1_VehicleYawRate_DegpS_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_SignlCondn.h`
- `filters.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
