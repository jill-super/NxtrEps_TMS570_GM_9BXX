---
title: "Return Output Firewall (ReturnFirewall)"
description: "Plausibility guard on the return-to-center assist path."
---

# Return Output Firewall

Directory: `ReturnFirewall` · AUTOSAR group: Application Software


## Purpose and responsibility

Plausibility guard on the return-to-center assist path.

## Source layout

Repository path: `ReturnFirewall/`

| File | Role |
| --- | --- |
| `ReturnFirewall/src/Ap_ReturnFirewall.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_ReturnFirewall_Per1_LimitedReturn_MtrNm_f32()`


## Dependencies

- `Ap_ReturnFirewall_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_ReturnFirewall.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
