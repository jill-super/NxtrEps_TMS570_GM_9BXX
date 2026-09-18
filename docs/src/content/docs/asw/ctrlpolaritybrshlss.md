---
title: "Control Polarity for Brushless Control (CtrlPolarityBrshlss)"
description: "Manages control polarity (sign conventions) for the brushless motor control path."
---

# Control Polarity for Brushless Control

Directory: `CtrlPolarityBrshlss` · AUTOSAR group: Application Software


## Purpose and responsibility

Manages control polarity (sign conventions) for the brushless motor control path.

## Source layout

Repository path: `CtrlPolarityBrshlss/`

| File | Role |
| --- | --- |
| `CtrlPolarityBrshlss/src/Ap_CtrlPolarityBrshlss.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Polarity_SCom_ReadPolarity()`
- `Polarity_SCom_SetPolarity()`


## Dependencies

- `MemMap.h`
- `Os.h`
- `Rte_Ap_CtrlPolarityBrshlss.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
