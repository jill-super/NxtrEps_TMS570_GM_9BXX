---
title: "Temporal Monitor for Dual Inverter (TmplMonrDualIvtr)"
description: "Temporal Monitor Function: continuously verifies that the dual-inverter control core executes correctly in time."
---

# Temporal Monitor for Dual Inverter

Directory: `TmplMonrDualIvtr` · AUTOSAR group: Application Software


## Purpose and responsibility

Temporal Monitor Function: continuously verifies that the dual-inverter control core executes correctly in time.

## Source layout

Repository path: `TmplMonrDualIvtr/`

| File | Role |
| --- | --- |
| `TmplMonrDualIvtr/src/Sa_TmplMonrDualIvtr.c` | Implementation |
| `TmplMonrDualIvtr/src/Sa_TmplMonrDualIvtr2.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_TmplMonrDualIvtr_Per2_TMFTestComplete_Cnt_lgc()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Sa_TmplMonrDualIvtr.h`
- `Rte_Sa_TmplMonrDualIvtr2.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
