---
title: "Serial Peripheral Interface Driver (SpiNxt)"
description: "Partial AUTOSAR Application Programming Interface implementation of the Serial Peripheral Interface driver, including interrupt service routines."
---

# Serial Peripheral Interface Driver

Directory: `SpiNxt` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Partial AUTOSAR Application Programming Interface implementation of the Serial Peripheral Interface driver, including interrupt service routines.

## Source layout

Repository path: `SpiNxt/`

| File | Role |
| --- | --- |
| `SpiNxt/src/SpiNxt.c` | Implementation |
| `SpiNxt/src/SpiNxt_Irq.c` | Implementation |
| `SpiNxt/include/SpiNxt.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `SpiNxt_IrqUnit2TxRx()`
- `SpiNxt_IrqUnit2TxRxERR()`
- `SpiNxt_Init()`
- `mibspiSetData()`
- `mibspiSetData8()`
- `mibspiSetCtrlData()`
- `mibspiGetData8()`
- `mibspiTransfer()`
- `mibspiEnableGroupNotification()`
- `mibspiNotification()`


## Dependencies

- `Dio.h`
- `MemMap.h`
- `Metrics.h`
- `Os.h`
- `SchM_SpiNxt.h`
- `SpiNxt.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
