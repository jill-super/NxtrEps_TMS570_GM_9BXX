---
title: "Over-Voltage Monitoring (OvrVoltMon)"
description: "Implements functional description FDD16: monitors the supply for over-voltage and triggers protection."
---

# Over-Voltage Monitoring

Directory: `OvrVoltMon` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements functional description FDD16: monitors the supply for over-voltage and triggers protection.

## Source layout

Repository path: `OvrVoltMon/`

| File | Role |
| --- | --- |
| `OvrVoltMon/src/Sa_OvrVoltMon.c` | Implementation |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Sa_OvrVoltMon.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
