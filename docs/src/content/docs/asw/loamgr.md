---
title: "Loss-of-Assist Management (LoaMgr)"
description: "Implements System Function SF49A: degrades gracefully and manages driver notification on loss of assist."
---

# Loss-of-Assist Management

Directory: `LoaMgr` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements System Function SF49A: degrades gracefully and manages driver notification on loss of assist.

## Source layout

Repository path: `LoaMgr/`

| File | Role |
| --- | --- |
| `LoaMgr/src/Ap_LoaMgr.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_LoaMgr_Per1_HwTqLoaMtgtnEn_Cnt_lgc()`
- `Rte_IWrite_LoaMgr_Per1_IvtrLoaMtgtnEn_Cnt_lgc()`
- `Rte_IWrite_LoaMgr_Per1_LOASt_State_enum()`
- `Rte_IWrite_LoaMgr_Per1_LoaRateLimit_UlspS_f32()`
- `Rte_IWrite_LoaMgr_Per1_LoaScaleFctr_Uls_f32()`
- `Rte_IWrite_LoaMgr_Per1_MotAgLoaMtgtnEn_Cnt_lgc()`
- `Rte_IWrite_LoaMgr_Per1_MotCurrLoaMtgtnEn_Cnt_lgc()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_LoaMgr.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
