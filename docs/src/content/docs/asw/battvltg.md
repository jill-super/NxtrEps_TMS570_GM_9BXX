---
title: "Battery Voltage Measurement and Arbitration (BattVltg)"
description: "Measures battery/switched voltage and arbitrates between redundant sources for consumers across the system."
---

# Battery Voltage Measurement and Arbitration

Directory: `BattVltg` · AUTOSAR group: Application Software


## Purpose and responsibility

Measures battery/switched voltage and arbitrates between redundant sources for consumers across the system.

## Source layout

Repository path: `BattVltg/`

| File | Role |
| --- | --- |
| `BattVltg/src/Ap_BattVltg.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_BattVltg_Init1_BrdgVltg_Volt_f32()`
- `Rte_IWrite_BattVltg_Per1_BrdgVltg_Volt_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_BattVltg.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
