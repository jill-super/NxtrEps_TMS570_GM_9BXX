---
title: "Battery Voltage Diagnostics (BVDiag)"
description: "Monitors battery voltage against over/under-voltage thresholds and reports diagnostic status to the Diagnostic Manager."
---

# Battery Voltage Diagnostics

Directory: `BVDiag` · AUTOSAR group: Application Software


## Purpose and responsibility

Monitors battery voltage against over/under-voltage thresholds and reports diagnostic status to the Diagnostic Manager.

## Source layout

Repository path: `BVDiag/`

| File | Role |
| --- | --- |
| `BVDiag/src/Ap_BVDiag.c` | Implementation |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `Ap_BVDiag_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_BVDiag.h`
- `SystemTime.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
