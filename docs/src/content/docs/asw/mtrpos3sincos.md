---
title: "Motor Position from Triple Sine-Cosine Sensors (MtrPos3SinCos)"
description: "Reconstructs motor position from three sine/cosine sensor bridges."
---

# Motor Position from Triple Sine-Cosine Sensors

Directory: `MtrPos3SinCos` · AUTOSAR group: Application Software


## Purpose and responsibility

Reconstructs motor position from three sine/cosine sensor bridges.

## Source layout

Repository path: `MtrPos3SinCos/`

| File | Role |
| --- | --- |
| `MtrPos3SinCos/src/Sa_MtrPos3SinCos.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_MtrPos3SinCos_Per1_MtrPos3Mech_Rev_u0p16()`
- `Rte_IWrite_MtrPos3SinCos_Per1_MtrPos3Qlfr_State_enum()`
- `Rte_IWrite_MtrPos3SinCos_Per1_MtrPos3RollgCntr_Cnt_u08()`
- `MtrPos3SinCos_Scom_ReadEOLMtrCals()`
- `MtrPos3SinCos_Scom_WriteEOLMtrCals()`


## Dependencies

- `CalConstants.h`
- `Crc.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Sa_MtrPos3SinCos.h`
- `atan2.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
