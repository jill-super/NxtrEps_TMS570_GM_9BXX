---
title: "Flash EEPROM Emulation Driver (Fee)"
description: "Texas Instruments Flash EEPROM Emulation driver for TMS570 (AUTOSAR Flash EEPROM Emulation 3.1 Application Programming Interface), adapted during integration at"
---

# Flash EEPROM Emulation Driver

Directory: `Fee` · AUTOSAR group: Microcontroller Abstraction

:::note[Origin: Third-party — Texas Instruments]
This module is third-party software supplied by Texas Instruments for the TMS570 microcontroller family. History entries show adaptations made at Vector's request during integration.
:::

## Purpose and responsibility

Texas Instruments Flash EEPROM Emulation driver for TMS570 (AUTOSAR Flash EEPROM Emulation 3.1 Application Programming Interface), adapted during integration at Vector's request.

## Source layout

Repository path: `Fee/`

| File | Role |
| --- | --- |
| `Fee/generate/Fee/T_Fee_Cfg.c` | Implementation |
| `Fee/src/Device_TMS570LS07.c` | Implementation |
| `Fee/src/Device_TMS570LS12.c` | Implementation |
| `Fee/src/fee.c` | Implementation |
| `Fee/src/ti_fee_Info.c` | Implementation |
| `Fee/src/ti_fee_cancel.c` | Implementation |
| `Fee/src/ti_fee_eraseimmediateblock.c` | Implementation |
| `Fee/src/ti_fee_format.c` | Implementation |
| `Fee/src/ti_fee_ini.c` | Implementation |
| `Fee/src/ti_fee_invalidateblock.c` | Implementation |
| `Fee/src/ti_fee_main.c` | Implementation |
| `Fee/src/ti_fee_read.c` | Implementation |
| `Fee/generate/Fee/T_Fee_Cfg.h` | Public header |
| `Fee/include/Device_Header.h` | Public header |
| `Fee/include/Device_TMS570LS07.h` | Public header |
| `Fee/include/Device_TMS570LS12.h` | Public header |
| `Fee/include/Device_types.h` | Public header |
| `Fee/include/Fee_Cbk.h` | Public header |
| `Fee/include/fee.h` | Public header |
| `Fee/include/fee_interface.h` | Public header |
| `Fee/include/fee_memmap.h` | Public header |
| `Fee/include/ti_fee.h` | Public header |
| `Fee/include/ti_fee_cfg.h` | Public header |
| `Fee/include/ti_fee_types.h` | Public header |


_Showing a selection; the directory holds 17 C files and 12 headers in total._


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `TI_Fee_GetVersionInfo()`
- `TI_Fee_Init()`


## Dependencies

- `Device_TMS570LS07.h`
- `Device_header.h`
- `MemMap.h`
- `ti_fee.h`


## Configuration and usage

Configured through the driver's own configuration headers and the integration project's memory/linker layout. See the [Microcontroller Abstraction overview](./).
