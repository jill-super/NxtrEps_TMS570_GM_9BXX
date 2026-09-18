---
title: "Vehicle Speed Limiting Interface (VehSpdLmt)"
description: "Interfaces vehicle-speed information and speed-dependent limiting into assist functions."
---

# Vehicle Speed Limiting Interface

Directory: `VehSpdLmt` · AUTOSAR group: Application Software


## Purpose and responsibility

Interfaces vehicle-speed information and speed-dependent limiting into assist functions.

## Source layout

Repository path: `VehSpdLmt/`

| File | Role |
| --- | --- |
| `VehSpdLmt/src/Ap_VehSpdLmt.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_VehSpdLmt_Per1_AstVehSpdLimit_MtrNm_f32()`


## Dependencies

- `Ap_VehSpdLmt_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_VehSpdLmt.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
