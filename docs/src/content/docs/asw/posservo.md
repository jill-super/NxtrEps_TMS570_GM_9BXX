---
title: "Position Servo Control (PosServo)"
description: "Closed-loop position servo used by scripted steering functions."
---

# Position Servo Control

Directory: `PosServo` · AUTOSAR group: Application Software


## Purpose and responsibility

Closed-loop position servo used by scripted steering functions.

## Source layout

Repository path: `PosServo/`

| File | Role |
| --- | --- |
| `PosServo/src/Ap_PosServo.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_PosServo_Per1_PosSrvoCmd_MtrNm_f32()`
- `Rte_IWrite_PosServo_Per1_PosSrvoReturnSclFct_Uls_f32()`
- `Rte_IWrite_PosServo_Per1_PosSrvoSmoothEnable_Uls_f32()`


## Dependencies

- `Ap_PosServo_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_PosServo.h`
- `SystemTime.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
