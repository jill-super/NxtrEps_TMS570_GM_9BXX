---
title: "Average Friction Learning (AvgFricLrn)"
description: "Learns the slowly-varying average friction of the steering system so assist and return functions can compensate it."
---

# Average Friction Learning

Directory: `AvgFricLrn` · AUTOSAR group: Application Software


## Purpose and responsibility

Learns the slowly-varying average friction of the steering system so assist and return functions can compensate it.

## Source layout

Repository path: `AvgFricLrn/`

| File | Role |
| --- | --- |
| `AvgFricLrn/src/Ap_AvgFricLrn.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_AvgFricLrn_Init1_FricOffset_HwNm_f32()`
- `Rte_IWrite_AvgFricLrn_Per1_EstFric_HwNm_f32()`
- `Rte_IWrite_AvgFricLrn_Per1_FricOffset_HwNm_f32()`
- `Rte_IWrite_AvgFricLrn_Per1_SatEstFric_HwNm_f32()`
- `AvgFricLrn_SCom_GetEOLFric()`
- `AvgFricLrn_SCom_GetOffsetOutputDefeat()`
- `AvgFricLrn_SCom_GetSelect()`
- `AvgFricLrn_SCom_InitLearnedTables()`
- `AvgFricLrn_SCom_ResetToZero()`
- `AvgFricLrn_SCom_SetEOLFric()`


## Dependencies

- `Ap_AvgFricLrn_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_AvgFricLrn.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
