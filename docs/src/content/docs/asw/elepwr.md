---
title: "Electrical Power Management (ElePwr)"
description: "Supervises electrical power distribution and power-stage enablement for the steering assist."
---

# Electrical Power Management

Directory: `ElePwr` · AUTOSAR group: Application Software


## Purpose and responsibility

Supervises electrical power distribution and power-stage enablement for the steering assist.

## Source layout

Repository path: `ElePwr/`

| File | Role |
| --- | --- |
| `ElePwr/src/Ap_ElePwr.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_ElePwr_Per1_ElectricPower_Watt_f32()`
- `Rte_IWrite_ElePwr_Per1_SupplyCurrent_Amp_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_ElePwr.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
