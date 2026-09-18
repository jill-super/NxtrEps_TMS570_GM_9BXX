---
title: "Motor Velocity from Digital Sensing (MtrVel_Digi)"
description: "Derives motor velocity from the digital position sensing path."
---

# Motor Velocity from Digital Sensing

Directory: `MtrVel_Digi` · AUTOSAR group: Application Software


## Purpose and responsibility

Derives motor velocity from the digital position sensing path.

## Source layout

Repository path: `MtrVel_Digi/`

| File | Role |
| --- | --- |
| `MtrVel_Digi/src/Sa_MtrVel.c` | Implementation |
| `MtrVel_Digi/src/Sa_MtrVel2.c` | Implementation |
| `MtrVel_Digi/src/Sa_MtrVel3.c` | Implementation |
| `MtrVel_Digi/include/Sa_MtrVel.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_MtrVel_Per1_HandwheelVel_HwRadpS_f32()`
- `Rte_IWrite_MtrVel_Per1_MotorVelCRF_MtrRadpS_f32()`
- `Rte_IWrite_MtrVel_Per1_MotorVelMRF_MtrRadpS_f32()`
- `Rte_IWrite_MtrVel_Per1_SysCHandwheelVel_HwRadpS_f32()`
- `Rte_IWrite_MtrVel_Per1_SysCMotorVelMRF_MtrRadpS_f32()`
- `Rte_IWrite_MtrVel_Per2_HwVelValid_Cnt_lgc()`
- `Rte_IWrite_MtrVel2_Per1_SysCDiagHwVel_HwRadpS_f32()`
- `Rte_IWrite_MtrVel2_Per1_SysCDiagMtrVelMRF_MtrRadpS_f32()`


## Dependencies

- `CalConstants.h`
- `Float.h`
- `GlobalMacro.h`
- `MemMap.h`
- `MtrVel_Cfg.h`
- `Rte_Sa_MtrVel.h`
- `Rte_Sa_MtrVel2.h`
- `Rte_Sa_MtrVel3.h`
- `Sa_MtrVel.h`
- `Sa_MtrVel2_Cfg.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
