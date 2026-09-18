---
title: "Handwheel Torque Arbitration (HwTrqArbn)"
description: "Implements the \"Hand Wheel Torque Arbitration\" function (engineering specification ES-56A): selects the valid torque signal among redundant sensors."
---

# Handwheel Torque Arbitration

Directory: `HwTrqArbn` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements the "Hand Wheel Torque Arbitration" function (engineering specification ES-56A): selects the valid torque signal among redundant sensors.

## Source layout

Repository path: `HwTrqArbn/`

| File | Role |
| --- | --- |
| `HwTrqArbn/src/Sa_HwTrqArbn.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_HwTrqArbn_Per1_ArbnAbsHwTqErr_HwNm_f32()`
- `Rte_IWrite_HwTrqArbn_Per1_HwTqVal_HwNm_f32()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Sa_HwTrqArbn.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
