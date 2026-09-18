---
title: "Damping Output Firewall (DampingFirewall)"
description: "Plausibility guard on the damping path (System Function SF35 family)."
---

# Damping Output Firewall

Directory: `DampingFirewall` · AUTOSAR group: Application Software


## Purpose and responsibility

Plausibility guard on the damping path (System Function SF35 family).

## Source layout

Repository path: `DampingFirewall/`

| File | Role |
| --- | --- |
| `DampingFirewall/src/Ap_DampingFirewall.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_DampingFirewall_Per1_CombinedDamping_MtrNm_f32()`


## Dependencies

- `Ap_DampingFirewall_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_DampingFirewall.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
