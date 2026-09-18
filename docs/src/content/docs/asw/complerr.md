---
title: "Component Error Handling (ComplErr)"
description: "Centralized handling of component-level error conditions reported by application functions. Assumption: short name expands to component/compliance error handlin"
---

# Component Error Handling

Directory: `ComplErr` · AUTOSAR group: Application Software


## Purpose and responsibility

Centralized handling of component-level error conditions reported by application functions. Assumption: short name expands to component/compliance error handling; the source file header is the normative reference.

## Source layout

Repository path: `ComplErr/`

| File | Role |
| --- | --- |
| `ComplErr/src/Ap_ComplErr.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_ComplErr_Per1_ComplErr_HwDeg_f32()`


## Dependencies

- `Ap_ComplErr_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_ComplErr.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
