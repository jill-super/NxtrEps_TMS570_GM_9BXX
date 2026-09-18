---
title: "Controller Temperature Monitoring (CtrlTemp)"
description: "Monitors power-stage/controller temperature and derates or protects the system on over-temperature."
---

# Controller Temperature Monitoring

Directory: `CtrlTemp` · AUTOSAR group: Application Software


## Purpose and responsibility

Monitors power-stage/controller temperature and derates or protects the system on over-temperature.

## Source layout

Repository path: `CtrlTemp/`

| File | Role |
| --- | --- |
| `CtrlTemp/src/Sa_CtrlTemp.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_CtrlTemp_Init1_FiltMeasTemp_DegC_f32()`
- `Rte_IWrite_CtrlTemp_Per1_FiltMeasTemp_DegC_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Sa_CtrlTemp.h`
- `Sa_CtrlTemp_Cfg.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
