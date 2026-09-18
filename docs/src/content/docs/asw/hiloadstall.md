---
title: "High-Load Stall Management (HiLoadStall)"
description: "Protects the motor and power stage against sustained high-load/stall operation."
---

# High-Load Stall Management

Directory: `HiLoadStall` · AUTOSAR group: Application Software


## Purpose and responsibility

Protects the motor and power stage against sustained high-load/stall operation.

## Source layout

Repository path: `HiLoadStall/`

| File | Role |
| --- | --- |
| `HiLoadStall/src/Ap_HiLoadStall.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_HiLoadStall_Per1_AssistStallLimit_MtrNm_f32()`


## Dependencies

- `Ap_HiLoadStall_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_HiLoadStall.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
