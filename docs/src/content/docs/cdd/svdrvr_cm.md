---
title: "Space-Vector Driver, Current Mode (SVDrvr_CM)"
description: "Non-AUTOSAR Pulse-Width Modulation driver that performs Electric Power Steering motor actuation via space-vector modulation. Assumption: suffix CM expands to Cu"
---

# Space-Vector Driver, Current Mode

Directory: `SVDrvr_CM` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Non-AUTOSAR Pulse-Width Modulation driver that performs Electric Power Steering motor actuation via space-vector modulation. Assumption: suffix CM expands to Current Mode.

## Source layout

Repository path: `SVDrvr_CM/`

| File | Role |
| --- | --- |
| `SVDrvr_CM/src/PwmCdd.c` | Implementation |
| `SVDrvr_CM/include/PwmCdd.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `CDD_Data.h`
- `CDD_Func.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `PwmCdd.h`
- `PwmCdd_Cfg.h`
- `fixmath.h`


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
