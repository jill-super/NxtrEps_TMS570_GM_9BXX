---
title: "Motor Mechanical Position 2 Sensing (MotMeclPosn2)"
description: "Acquisition and qualification of motor mechanical position channel 2 (redundant channel)."
---

# Motor Mechanical Position 2 Sensing

Directory: `MotMeclPosn2` · AUTOSAR group: Application Software


## Purpose and responsibility

Acquisition and qualification of motor mechanical position channel 2 (redundant channel).

## Source layout

Repository path: `MotMeclPosn2/`

| File | Role |
| --- | --- |
| `MotMeclPosn2/src/Sa_MotMeclPosn2.c` | Implementation |
| `MotMeclPosn2/include/Sa_MotMeclPosn2.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_MotMeclPosn2_Per2_MotPosnQlfr_State_enum()`
- `MotMeclPosn2_Scom_ReadMotMeclPosn2CoeffTbl()`
- `MotMeclPosn2_Scom_WriteMotMeclPosn2CoeffTbl()`


## Dependencies

- `Crc.h`
- `GlobalMacro.h`
- `MemMap.h`
- `MotMeclPosn2_Cfg.h`
- `Rte_Sa_MotMeclPosn2.h`
- `Sa_MotMeclPosn2.h`
- `SinCos.h`
- `SystemTime.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
