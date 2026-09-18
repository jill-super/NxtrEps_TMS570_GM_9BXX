---
title: "Enhanced Pulse-Width Modulation Setup (ePWM_Up)"
description: "Implements the \"Motor Control Configuration Override\" subfunction of engineering specification ES-34E on the Enhanced Pulse-Width Modulation peripheral."
---

# Enhanced Pulse-Width Modulation Setup

Directory: `ePWM_Up` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Implements the "Motor Control Configuration Override" subfunction of engineering specification ES-34E on the Enhanced Pulse-Width Modulation peripheral.

## Source layout

Repository path: `ePWM_Up/`

| File | Role |
| --- | --- |
| `ePWM_Up/src/Ap_ePWM2.c` | Implementation |
| `ePWM_Up/src/ePWM.c` | Implementation |
| `ePWM_Up/include/ePWM.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_ePWM2.h`
- `ePWM_Cfg.h`
- `ePwm.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
