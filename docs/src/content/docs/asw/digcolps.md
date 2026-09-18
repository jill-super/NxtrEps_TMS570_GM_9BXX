---
title: "Digital Column Position Sensing (DigColPs)"
description: "Digital steering-column position acquisition and qualification."
---

# Digital Column Position Sensing

Directory: `DigColPs` · AUTOSAR group: Application Software


## Purpose and responsibility

Digital steering-column position acquisition and qualification.

## Source layout

Repository path: `DigColPs/`

| File | Role |
| --- | --- |
| `DigColPs/src/Sa_DigColPs.c` | Implementation |
| `DigColPs/src/Sa_DigColPsInt.c` | Implementation |
| `DigColPs/include/Sa_DigColPsInt.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_DigColPs_Per2_I2CHwAbsPosValid_Cnt_lgc()`
- `Rte_IWrite_DigColPs_Per2_I2CHwAbsPos_HwDeg_f32()`
- `Rte_IWrite_DigColPs_Per2_TrimComp_Cnt_lgc()`
- `DigColPs_SCom_CustClrTrim()`
- `DigColPs_SCom_NxtClrTrim()`
- `PhaNvmRead_GetData()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `I2cNxtr.h`
- `I2cNxtr_Cfg.h`
- `MemMap.h`
- `Os.h`
- `Rte_Sa_DigColPs.h`
- `Sa_DigColPsInt.h`
- `SystemTime.h`
- `filters.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
