---
title: "Motor Phase Feedback Measurement (PhaseFdbkMeas)"
description: "Phase-feedback measurement for motor control (engineering specification ES36A, functional description FDD), including High-End Timer capture programming."
---

# Motor Phase Feedback Measurement

Directory: `PhaseFdbkMeas` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Phase-feedback measurement for motor control (engineering specification ES36A, functional description FDD), including High-End Timer capture programming.

## Source layout

Repository path: `PhaseFdbkMeas/`

| File | Role |
| --- | --- |
| `PhaseFdbkMeas/src/Cd_PhaseFdbkMeas.c` | Implementation |
| `PhaseFdbkMeas/src/Nhet_PhaseFdbkMeas_Prog.c` | Implementation |
| `PhaseFdbkMeas/include/Cd_PhaseFdbkMeas.h` | Public header |
| `PhaseFdbkMeas/include/Nhet_PhaseFdbkMeas_Prog.h` | Public header |
| `PhaseFdbkMeas/include/std_nhet.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_Cd_PhaseFdbkMeas_Per1_MeasuredOnTimeA_Cnt_u32()`
- `Rte_IWrite_Cd_PhaseFdbkMeas_Per1_MeasuredOnTimeB_Cnt_u32()`
- `Rte_IWrite_Cd_PhaseFdbkMeas_Per1_MeasuredOnTimeC_Cnt_u32()`
- `Rte_IWrite_Cd_PhaseFdbkMeas_Per1_MeasuredOnTimeD_Cnt_u32()`
- `Rte_IWrite_Cd_PhaseFdbkMeas_Per1_MeasuredOnTimeE_Cnt_u32()`
- `Rte_IWrite_Cd_PhaseFdbkMeas_Per1_MeasuredOnTimeF_Cnt_u32()`
- `Get_PhaseFdbk_PhaseFdbk()`


## Dependencies

- `Cd_PhaseFdbkMeas.h`
- `MemMap.h`
- `Rte_Cd_PhaseFdbkMeas.h`
- `std_nhet.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
