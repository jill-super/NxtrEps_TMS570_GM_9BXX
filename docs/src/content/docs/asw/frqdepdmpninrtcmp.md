---
title: "Frequency-Dependent Damping and Inertia Compensation (FrqDepDmpnInrtCmp)"
description: "Shapes damping and compensates steering inertia as a function of excitation frequency."
---

# Frequency-Dependent Damping and Inertia Compensation

Directory: `FrqDepDmpnInrtCmp` · AUTOSAR group: Application Software


## Purpose and responsibility

Shapes damping and compensates steering inertia as a function of excitation frequency.

## Source layout

Repository path: `FrqDepDmpnInrtCmp/`

| File | Role |
| --- | --- |
| `FrqDepDmpnInrtCmp/src/Ap_FrqDepDmpnInrtCmp.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_FrqDepDmpnInrtCmp_Per1_FrqDepDmpnInrtCmp_MtrNm_f32()`


## Dependencies

- `Ap_FrqDepDmpnInrtCmp_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_FrqDepDmpnInrtCmp.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
