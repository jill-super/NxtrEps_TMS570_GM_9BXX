---
title: "End-of-Travel Damping Firewall (EtDmpFw)"
description: "Firewall guarding the end-of-travel damping output. Assumption: short name expands to End-of-Travel Damping Firewall; the source file header is normative."
---

# End-of-Travel Damping Firewall

Directory: `EtDmpFw` · AUTOSAR group: Application Software


## Purpose and responsibility

Firewall guarding the end-of-travel damping output. Assumption: short name expands to End-of-Travel Damping Firewall; the source file header is normative.

## Source layout

Repository path: `EtDmpFw/`

| File | Role |
| --- | --- |
| `EtDmpFw/src/Ap_EtDmpFw.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_EtDmpFw_Per1_EOTDampingLtd_MtrNm_f32()`


## Dependencies

- `Ap_EtDmpFw_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_EtDmpFw.h`
- `fixmath.h`
- `fpmtype.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
