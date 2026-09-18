---
title: "Non-Volatile Memory Proxy (NvMProxy)"
description: "Complex Driver acting as a proxy between application Software Components and the Non-Volatile Memory stack."
---

# Non-Volatile Memory Proxy

Directory: `NvMProxy` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Complex Driver acting as a proxy between application Software Components and the Non-Volatile Memory stack.

## Source layout

Repository path: `NvMProxy/`

| File | Role |
| --- | --- |
| `NvMProxy/src/Cd_NvMProxy.c` | Implementation |
| `NvMProxy/include/Cd_NvMProxy.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `Cd_NvMProxy.h`
- `Crc.h`
- `MemMap.h`
- `NvM.h`
- `SchM_NvMProxy.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
