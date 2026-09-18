---
title: "Motor Temperature Estimation (MtrTempEst)"
description: "Estimates motor winding/magnet temperature from models and measurements for derating and protection."
---

# Motor Temperature Estimation

Directory: `MtrTempEst` · AUTOSAR group: Application Software


## Purpose and responsibility

Estimates motor winding/magnet temperature from models and measurements for derating and protection.

## Source layout

Repository path: `MtrTempEst/`

| File | Role |
| --- | --- |
| `MtrTempEst/src/Ap_MtrTempEst.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_MtrTempEst_Init1_AssistMechTempEst_DegC_f32()`
- `Rte_IWrite_MtrTempEst_Init1_CuTempEst_DegC_f32()`
- `Rte_IWrite_MtrTempEst_Init1_MagTempEst_DegC_f32()`
- `Rte_IWrite_MtrTempEst_Init1_SiTempEst_DegC_f32()`
- `Rte_IWrite_MtrTempEst_Per1_AssistMechTempEst_DegC_f32()`
- `Rte_IWrite_MtrTempEst_Per1_CuTempEst_DegC_f32()`
- `Rte_IWrite_MtrTempEst_Per1_MagTempEst_DegC_f32()`
- `Rte_IWrite_MtrTempEst_Per1_SiTempEst_DegC_f32()`


## Dependencies

- `Ap_MtrTempEst_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_MtrTempEst.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
