---
title: "Digital Motor Position Sensor Arbitration (DigMSBArbn)"
description: "Non-AUTOSAR helper that checks signal availability of Motor Position 1 and 2 and forwards whichever is valid (preferring Motor Position 1)."
---

# Digital Motor Position Sensor Arbitration

Directory: `DigMSBArbn` · AUTOSAR group: Application Software


## Purpose and responsibility

Non-AUTOSAR helper that checks signal availability of Motor Position 1 and 2 and forwards whichever is valid (preferring Motor Position 1).

## Source layout

Repository path: `DigMSBArbn/`

| File | Role |
| --- | --- |
| `DigMSBArbn/src/Sa_DigMSBArbn.c` | Implementation |
| `DigMSBArbn/include/Sa_DigMSBArbn.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `CalConstants.h`
- `DigMSBArbn_Cfg.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Platform_Types.h`
- `Rte_Type.h`
- `Sa_DigMSBArbn.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
