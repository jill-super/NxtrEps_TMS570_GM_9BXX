---
title: "Motor Mechanical Position 1 Sensing (MotMeclPosn1)"
description: "Acquisition and qualification of motor mechanical position channel 1."
---

# Motor Mechanical Position 1 Sensing

Directory: `MotMeclPosn1` · AUTOSAR group: Application Software


## Purpose and responsibility

Acquisition and qualification of motor mechanical position channel 1.

## Source layout

Repository path: `MotMeclPosn1/`

| File | Role |
| --- | --- |
| `MotMeclPosn1/src/Sa_MotMeclPosn1.c` | Implementation |
| `MotMeclPosn1/include/Sa_MotMeclPosn1.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_MotMeclPosn1_Per2_MotPosnQlfr_State_enum()`
- `MotMeclPosn1_Scom_ReadMotMeclPosn1CoeffTbl()`
- `MotMeclPosn1_Scom_WriteMotMeclPosn1CoeffTbl()`


## Dependencies

- `Crc.h`
- `GlobalMacro.h`
- `MemMap.h`
- `MotMeclPosn1_Cfg.h`
- `Rte_Sa_MotMeclPosn1.h`
- `Sa_MotMeclPosn1.h`
- `SinCos.h`
- `SystemTime.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
