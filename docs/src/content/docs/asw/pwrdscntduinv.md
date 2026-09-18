---
title: "Power Disconnect for Dual Inverter (PwrDscntDuInv)"
description: "Controls the power disconnect path of the dual-inverter power stage (legacy of ES011C)."
---

# Power Disconnect for Dual Inverter

Directory: `PwrDscntDuInv` · AUTOSAR group: Application Software


## Purpose and responsibility

Controls the power disconnect path of the dual-inverter power stage (legacy of ES011C).

## Source layout

Repository path: `PwrDscntDuInv/`

| File | Role |
| --- | --- |
| `PwrDscntDuInv/src/Ap_PwrDscntDuInv.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_PwrDscntDuInv_Per1_PwrDiscATestComplete_Cnt_lgc()`
- `Rte_IWrite_PwrDscntDuInv_Per1_PwrDiscBTestComplete_Cnt_lgc()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_PwrDscntDuInv.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
