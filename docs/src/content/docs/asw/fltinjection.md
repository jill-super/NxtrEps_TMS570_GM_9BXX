---
title: "Fault Injection Test Support (FltInjection)"
description: "Test-only hooks to inject faults and verify diagnostic reactions. Not part of the production control path."
---

# Fault Injection Test Support

Directory: `FltInjection` · AUTOSAR group: Application Software


## Purpose and responsibility

Test-only hooks to inject faults and verify diagnostic reactions. Not part of the production control path.

## Source layout

Repository path: `FltInjection/`

| File | Role |
| --- | --- |
| `FltInjection/src/Ap_FltInjection.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `FltInjection_SCom_FltInjection()`


## Dependencies

- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_FltInjection.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
