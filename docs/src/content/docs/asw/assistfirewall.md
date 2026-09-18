---
title: "Assist Output Firewall (AssistFirewall)"
description: "Plausibility guard on the assist path: limits/freezes the assist command when upstream signals are invalid."
---

# Assist Output Firewall

Directory: `AssistFirewall` · AUTOSAR group: Application Software


## Purpose and responsibility

Plausibility guard on the assist path: limits/freezes the assist command when upstream signals are invalid.

## Source layout

Repository path: `AssistFirewall/`

| File | Role |
| --- | --- |
| `AssistFirewall/src/Ap_AssistFirewall.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_AssistFirewall_Per1_AsstFirewallActive_Uls_f32()`
- `Rte_IWrite_AssistFirewall_Per1_CombinedAssist_MtrNm_f32()`


## Dependencies

- `Ap_AssistFirewall_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_AssistFirewall.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
