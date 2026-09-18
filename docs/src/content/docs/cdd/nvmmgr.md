---
title: "Non-Volatile Memory Manager (NvMMgr)"
description: "Fee-interface Complex Driver (Cd_FeeIf): thin in-house manager above the Flash EEPROM Emulation driver, plus Flash Application Programming Interface user-define"
---

# Non-Volatile Memory Manager

Directory: `NvMMgr` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Fee-interface Complex Driver (Cd_FeeIf): thin in-house manager above the Flash EEPROM Emulation driver, plus Flash Application Programming Interface user-defined functions.

## Source layout

Repository path: `NvMMgr/`

| File | Role |
| --- | --- |
| `NvMMgr/src/Cd_FeeIf.c` | Implementation |
| `NvMMgr/src/Fapi_UserDefinedFunctions.c` | Implementation |
| `NvMMgr/include/Cd_FeeIf.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `TWrapC_FeeIf_Init()`
- `TRUSTED_TWrapS_FeeIf_Init()`
- `TWrapC_Fee_MainFunction()`
- `TRUSTED_TWrapS_Fee_MainFunction()`
- `TRUSTED_TWrapS_Fee_Read()`
- `TRUSTED_TWrapS_Fee_Write()`
- `TRUSTED_TWrapS_Fee_EraseImmediateBlock()`
- `TRUSTED_TWrapS_Fee_InvalidateBlock()`
- `TWrapC_Fee_Cancel()`
- `TRUSTED_TWrapS_Fee_Cancel()`


## Dependencies

- `Cd_FeeIf.h`
- `F021.h`


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
