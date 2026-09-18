---
title: "System State Manager (StaMd)"
description: "Core states-and-modes component: owns the system state machine and state-transition vectors (off, operate, warm-init transitions)."
---

# System State Manager

Directory: `StaMd` · AUTOSAR group: Application Software


## Purpose and responsibility

Core states-and-modes component: owns the system state machine and state-transition vectors (off, operate, warm-init transitions).

## Source layout

Repository path: `StaMd/`

| File | Role |
| --- | --- |
| `StaMd/src/Ap_StaMd.c` | Implementation |
| `StaMd/include/Ap_StaMd.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `Ap_StaMd_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Os.h`
- `Rte_Ap_StaMd.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
