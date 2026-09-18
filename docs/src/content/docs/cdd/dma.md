---
title: "Direct Memory Access Driver (Dma)"
description: "Direct Memory Access peripheral driver used for hardware-triggered data moves without Central Processing Unit intervention."
---

# Direct Memory Access Driver

Directory: `Dma` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Direct Memory Access peripheral driver used for hardware-triggered data moves without Central Processing Unit intervention.

## Source layout

Repository path: `Dma/`

| File | Role |
| --- | --- |
| `Dma/src/Dma.c` | Implementation |
| `Dma/include/Dma.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `Dma.h`
- `MemMap.h`
- `dma_regs.h`


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
