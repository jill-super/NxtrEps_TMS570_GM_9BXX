---
title: "Base Power Assist Control (Assist)"
description: "Core power-assist computation: converts driver handwheel torque and vehicle state into the base motor assist command."
---

# Base Power Assist Control

Directory: `Assist` · AUTOSAR group: Application Software


## Purpose and responsibility

Core power-assist computation: converts driver handwheel torque and vehicle state into the base motor assist command.

## Source layout

Repository path: `Assist/`

| File | Role |
| --- | --- |
| `Assist/src/Ap_Assist.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_Assist_Per1_BaseAssistCmd_MtrNm_f32()`


## Dependencies

- `Ap_Assist_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_Assist.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
