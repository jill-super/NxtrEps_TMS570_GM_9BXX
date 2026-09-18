---
title: "Shutdown Mechanism (ShtdnMech)"
description: "Coordinates orderly shutdown of assist and power stage on critical faults."
---

# Shutdown Mechanism

Directory: `ShtdnMech` · AUTOSAR group: Application Software


## Purpose and responsibility

Coordinates orderly shutdown of assist and power stage on critical faults.

## Source layout

Repository path: `ShtdnMech/`

| File | Role |
| --- | --- |
| `ShtdnMech/src/Sa_ShtdnMech.c` | Implementation |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `MemMap.h`
- `Rte_Sa_ShtdnMech.h`
- `Sa_ShtdnMech_Cfg.h`
- `n2het_regs.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
