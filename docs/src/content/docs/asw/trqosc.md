---
title: "Torque Oscillation Control (TrqOsc)"
description: "Suppresses torque oscillations in the steering chain."
---

# Torque Oscillation Control

Directory: `TrqOsc` · AUTOSAR group: Application Software


## Purpose and responsibility

Suppresses torque oscillations in the steering chain.

## Source layout

Repository path: `TrqOsc/`

| File | Role |
| --- | --- |
| `TrqOsc/src/Ap_TrqOsc.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_TrqOsc_Per1_TrqOscCmd_MtrNm_f32()`
- `Rte_IWrite_TrqOsc_Per1_TrqOscDCExceeded_Cnt_lgc()`


## Dependencies

- `Ap_TrqOsc_Cfg.h`
- `CalConstants.h`
- `MemMap.h`
- `Rte_Ap_TrqOsc.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
