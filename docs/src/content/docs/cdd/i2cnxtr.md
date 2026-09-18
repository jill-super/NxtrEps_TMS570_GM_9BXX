---
title: "Inter-Integrated Circuit Driver (I2cNxtr)"
description: "Nexteer implementation of the Inter-Integrated Circuit driver, including interrupt service routines."
---

# Inter-Integrated Circuit Driver

Directory: `I2cNxtr` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Nexteer implementation of the Inter-Integrated Circuit driver, including interrupt service routines.

## Source layout

Repository path: `I2cNxtr/`

| File | Role |
| --- | --- |
| `I2cNxtr/src/I2cNxtr.c` | Implementation |
| `I2cNxtr/src/I2cNxtr_Irq.c` | Implementation |
| `I2cNxtr/include/I2cNxtr.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `I2cNxtr.h`
- `I2cNxtr_Cfg.h`
- `MemMap.h`
- `Metrics.h`
- `Os.h`
- `SystemTime.h`
- `interrupts.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
