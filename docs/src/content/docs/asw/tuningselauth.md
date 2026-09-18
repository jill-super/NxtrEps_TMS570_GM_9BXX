---
title: "Tuning Selection Authorization (TuningSelAuth)"
description: "Authorizes which calibration/tuning set is active (e.g., tune-on-the-fly segments)."
---

# Tuning Selection Authorization

Directory: `TuningSelAuth` · AUTOSAR group: Application Software


## Purpose and responsibility

Authorizes which calibration/tuning set is active (e.g., tune-on-the-fly segments).

## Source layout

Repository path: `TuningSelAuth/`

| File | Role |
| --- | --- |
| `TuningSelAuth/src/Ap_TuningSelAuth.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_TuningSelAuth_Init1_ActiveTunPers_Cnt_u16()`
- `Rte_IWrite_TuningSelAuth_Init1_ActiveTunSet_Cnt_u16()`
- `Rte_IWrite_TuningSelAuth_Per1_ActiveTunPers_Cnt_u16()`
- `Rte_IWrite_TuningSelAuth_Per1_ActiveTunSet_Cnt_u16()`


## Dependencies

- `Ap_TuningSelAuth_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_TuningSelAuth.h`
- `XcpProf.h`
- `filters.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
