---
title: "Torque Overlay State, Customer Feature 09 (TrqOvlSta)"
description: "Implements customer feature CF09: torque overlay state handling for driver-assistance overlays."
---

# Torque Overlay State, Customer Feature 09

Directory: `TrqOvlSta` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements customer feature CF09: torque overlay state handling for driver-assistance overlays.

## Source layout

Repository path: `TrqOvlSta/`

| File | Role |
| --- | --- |
| `TrqOvlSta/src/Ap_TrqOvlSta.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_TrqOvlSta_Per1_APADrvrInterventionDetected_Cnt_lgc()`
- `Rte_IWrite_TrqOvlSta_Per1_APAState_State_enum()`
- `Rte_IWrite_TrqOvlSta_Per1_ESCState_State_enum()`
- `Rte_IWrite_TrqOvlSta_Per1_GMOSHOscillateState_State_enum()`
- `Rte_IWrite_TrqOvlSta_Per1_LKAState_State_enum()`
- `Rte_IWrite_TrqOvlSta_Per1_LkaDrvrIntvDetd_Cnt_lgc()`
- `Rte_IWrite_TrqOvlSta_Per1_PosServEnable_Cnt_lgc()`
- `Rte_IWrite_TrqOvlSta_Per1_PosSrvoHwAngle_HwDeg_f32()`
- `Rte_IWrite_TrqOvlSta_Per1_TrqOscAmp_MtrNm_f32()`
- `Rte_IWrite_TrqOvlSta_Per1_TrqOscEnable_Cnt_lgc()`


## Dependencies

- `Ap_TrqOvlSta_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `Interpolation.h`
- `MemMap.h`
- `Rte_Ap_TrqOvlSta.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
