---
title: "Wheel Imbalance Rejection (WhlImbRej)"
description: "Rejects wheel-imbalance-induced vibration from the steering feel."
---

# Wheel Imbalance Rejection

Directory: `WhlImbRej` · AUTOSAR group: Application Software


## Purpose and responsibility

Rejects wheel-imbalance-induced vibration from the steering feel.

## Source layout

Repository path: `WhlImbRej/`

| File | Role |
| --- | --- |
| `WhlImbRej/src/Ap_WhlImbRej.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_WhlImbRej_Per1_WIRCmdAmpBlnd_MtrNm_f32()`
- `Rte_IWrite_WhlImbRej_Per1_WhlImbRejCmd_MtrNm_f32()`
- `Rte_IWrite_WhlImbRej_Per3_WhlImbRejCmd_MtrNm_f32()`
- `WhlImbRej_SCom_GetWIRInfo()`


## Dependencies

- `Ap_WhlImbRej_Cfg.h`
- `CalConstants.h`
- `Filter_Types.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_WhlImbRej.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
