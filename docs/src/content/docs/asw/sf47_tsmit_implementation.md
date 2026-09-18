---
title: "Torque Disturbance Mitigation, System Function 47 (SF47_TSMit_Implementation)"
description: "Provides a motor torque command that mitigates linear rack-force disturbances (torsional vibration mitigation)."
---

# Torque Disturbance Mitigation, System Function 47

Directory: `SF47_TSMit_Implementation` · AUTOSAR group: Application Software


## Purpose and responsibility

Provides a motor torque command that mitigates linear rack-force disturbances (torsional vibration mitigation).

## Source layout

Repository path: `SF47_TSMit_Implementation/`

| File | Role |
| --- | --- |
| `SF47_TSMit_Implementation/src/Ap_TSMit.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_TSMit_Per1_TSMitCommand_MtrNm_f32()`
- `Rte_IWrite_TSMit_Per1_TSMitLearningEnabled_Cnt_lgc()`
- `TSMit_SCom_GainReset()`
- `TSMit_SCom_GetFcnDefeat()`
- `TSMit_SCom_GetLongTermGains()`
- `TSMit_SCom_GetLrnDefeat()`
- `TSMit_SCom_SetFcnDefeat()`
- `TSMit_SCom_SetLongTermGains()`
- `TSMit_SCom_SetLrnDefeat()`


## Dependencies

- `Ap_TSMit_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_TSMit.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
