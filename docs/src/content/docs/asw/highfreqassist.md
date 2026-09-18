---
title: "High-Frequency Assist (HighFreqAssist)"
description: "High-frequency component of the assist control for responsiveness and vibration behavior."
---

# High-Frequency Assist

Directory: `HighFreqAssist` · AUTOSAR group: Application Software


## Purpose and responsibility

High-frequency component of the assist control for responsiveness and vibration behavior.

## Source layout

Repository path: `HighFreqAssist/`

| File | Role |
| --- | --- |
| `HighFreqAssist/src/Ap_HighFreqAssist.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_HighFreqAssist_Per1_HighFreqAssist_MtrNm_f32()`


## Dependencies

- `Ap_HighFreqAssist_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_HighFreqAssist.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
