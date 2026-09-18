---
title: "Frequency Sweep Excitation (Sweep)"
description: "Generates frequency-sweep excitation for diagnostics and system identification."
---

# Frequency Sweep Excitation

Directory: `Sweep` · AUTOSAR group: Application Software


## Purpose and responsibility

Generates frequency-sweep excitation for diagnostics and system identification.

## Source layout

Repository path: `Sweep/`

| File | Role |
| --- | --- |
| `Sweep/src/Ap_Sweep.c` | Implementation |
| `Sweep/src/Ap_Sweep2.c` | Implementation |
| `Sweep/include/Ap_Sweep.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_Sweep_Per1_OutputHwTrq_HwNm_f32()`
- `Rte_IWrite_Sweep2_Per1_OutputMtrTrq_MtrNm_f32()`


## Dependencies

- `Ap_Sweep.h`
- `Ap_Sweep2_Cfg.h`
- `Ap_Sweep_Cfg.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_Sweep.h`
- `Rte_Ap_Sweep2.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
