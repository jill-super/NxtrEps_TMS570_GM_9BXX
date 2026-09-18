---
title: "Controlled Velocity Return (CtrldVelRtn)"
description: "Implements System Function SF002B: actively returns the steering toward center with a controlled velocity profile."
---

# Controlled Velocity Return

Directory: `CtrldVelRtn` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements System Function SF002B: actively returns the steering toward center with a controlled velocity profile.

## Source layout

Repository path: `CtrldVelRtn/`

| File | Role |
| --- | --- |
| `CtrldVelRtn/src/CtrldVelRtn.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_CtrldVelRtn_Per1_ReturnCmd_MtrNm_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_CtrldVelRtn.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
