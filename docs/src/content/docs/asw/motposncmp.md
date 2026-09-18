---
title: "Motor Position Compensation (MotPosnCmp)"
description: "Compensates systematic motor position errors before use by control and diagnostics."
---

# Motor Position Compensation

Directory: `MotPosnCmp` · AUTOSAR group: Application Software


## Purpose and responsibility

Compensates systematic motor position errors before use by control and diagnostics.

## Source layout

Repository path: `MotPosnCmp/`

| File | Role |
| --- | --- |
| `MotPosnCmp/src/Ap_MotPosnCmp.c` | Implementation |
| `MotPosnCmp/include/Ap_MotPosnCmp.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_MotPosnCmp_Per2_MotPosnCumvAlgndCrf_Deg_f32()`
- `Rte_IWrite_MotPosnCmp_Per2_MotPosnCumvAlgndMrf_Deg_f32()`
- `MotPosnCmp_Scom_MotPosnCmpBackEmfRead()`
- `MotPosnCmp_Scom_MotPosnCmpBackEmfWr()`


## Dependencies

- `Ap_MotPosnCmp.h`
- `Crc.h`
- `GlobalMacro.h`
- `MemMap.h`
- `MotPosnCmp_Cfg.h`
- `Rte_Ap_MotPosnCmp.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
