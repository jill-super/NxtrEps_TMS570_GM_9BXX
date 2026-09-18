---
title: "Powerpack Service Data Recovery (GmPwrpkSrvDataRcvry_CF034B)"
description: "Implements customer feature CF034B: recovery of powerpack service data."
---

# Powerpack Service Data Recovery

Directory: `GmPwrpkSrvDataRcvry_CF034B` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements customer feature CF034B: recovery of powerpack service data.

## Source layout

Repository path: `GmPwrpkSrvDataRcvry_CF034B/`

| File | Role |
| --- | --- |
| `GmPwrpkSrvDataRcvry_CF034B/src/Ap_GmPwrpkSrvDataRcvry.c` | Implementation |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_GmPwrpkSrvDataRcvry.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
