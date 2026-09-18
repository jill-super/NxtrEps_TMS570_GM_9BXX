---
title: "High-End Timer Module 1 Configuration and Use (Nhet1CfgAndUse)"
description: "Implements engineering specification ES-35B: configuration and use of the TMS570 High-End Timer (NHET1) peripheral."
---

# High-End Timer Module 1 Configuration and Use

Directory: `Nhet1CfgAndUse` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Implements engineering specification ES-35B: configuration and use of the TMS570 High-End Timer (NHET1) peripheral.

## Source layout

Repository path: `Nhet1CfgAndUse/`

| File | Role |
| --- | --- |
| `Nhet1CfgAndUse/src/Cd_Nhet1CfgAndUse.c` | Implementation |
| `Nhet1CfgAndUse/src/Nhet1CfgAndUse_Prog.c` | Implementation |
| `Nhet1CfgAndUse/include/Cd_Nhet1CfgAndUse.h` | Public header |
| `Nhet1CfgAndUse/include/Nhet.h` | Public header |
| `Nhet1CfgAndUse/include/Nhet1CfgAndUse_Prog.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_Nhet1CfgAndUse_Per2_HwTq3Qlfr_State_enum()`
- `Rte_IWrite_Nhet1CfgAndUse_Per2_HwTq3RollgCntr_Cnt_u08()`
- `Rte_IWrite_Nhet1CfgAndUse_Per2_HwTq3Val_HwNm_f32()`
- `Rte_IWrite_Nhet1CfgAndUse_Per2_HwTq4Qlfr_State_enum()`
- `Rte_IWrite_Nhet1CfgAndUse_Per2_HwTq4RollgCntr_Cnt_u08()`
- `Rte_IWrite_Nhet1CfgAndUse_Per2_HwTq4Val_HwNm_f32()`


## Dependencies

- `CalConstants.h`
- `Cd_Nhet1CfgAndUse.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Nhet1CfgAndUse_Cfg.h`
- `Rte_Cd_Nhet1CfgAndUse.h`
- `std_nhet.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
