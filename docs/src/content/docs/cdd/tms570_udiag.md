---
title: "Microcontroller Diagnostics (TMS570_uDiag)"
description: "Micro-level diagnostics Complex Driver (Cd_uDiag): supervises TMS570 safety mechanisms such as the Vectored Interrupt Manager, Error Signaling Module, clock mon"
---

# Microcontroller Diagnostics

Directory: `TMS570_uDiag` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Micro-level diagnostics Complex Driver (Cd_uDiag): supervises TMS570 safety mechanisms such as the Vectored Interrupt Manager, Error Signaling Module, clock monitors, and Error Correcting Code logic.

## Source layout

Repository path: `TMS570_uDiag/`

| File | Role |
| --- | --- |
| `TMS570_uDiag/src/AbortHandler.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagCCRM.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagClockMonitor.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagECC.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagESM.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagFPU.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagIOMM.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagLossOfExec.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagParity.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagPeriphMPU.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagResetHandler.c` | Implementation |
| `TMS570_uDiag/src/Cd_uDiagStaticRegs.c` | Implementation |
| `TMS570_uDiag/include/Cd_uDiagUtility.h` | Public header |
| `TMS570_uDiag/include/FlsTst.h` | Public header |
| `TMS570_uDiag/include/RednRpdShtdn.h` | Public header |
| `TMS570_uDiag/include/uDiag.h` | Public header |


_Showing a selection; the directory holds 18 C files and 4 headers in total._


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `VIM_Fallback()`
- `TWrapC_uDiagVIM_RednRpdShtdn()`
- `TRUSTED_TWrapS_uDiagVIM_RednRpdShtdn()`
- `Mcu_FpuIrq()`


## Dependencies

- `Ap_DiagMgr.h`
- `CalConstants.h`
- `Cd_uDiagUtility.h`
- `Dma.h`
- `Interrupts.h`
- `MemMap.h`
- `Nhet.h`
- `Os.h`
- `RednRpdShtdn.h`
- `ResetCause.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
