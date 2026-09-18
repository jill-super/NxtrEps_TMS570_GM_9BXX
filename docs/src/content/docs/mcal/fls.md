---
title: "Flash Memory Driver (Fls)"
description: "Texas Instruments F021 Flash Application Programming Interface library for Cortex-R4 (big-endian build used here) with compiler-abstraction headers."
---

# Flash Memory Driver

Directory: `Fls` · AUTOSAR group: Microcontroller Abstraction

:::note[Origin: Third-party — Texas Instruments]
This module is third-party software supplied by Texas Instruments for the TMS570 microcontroller family. History entries show adaptations made at Vector's request during integration.
:::

## Purpose and responsibility

Texas Instruments F021 Flash Application Programming Interface library for Cortex-R4 (big-endian build used here) with compiler-abstraction headers.

## Source layout

Repository path: `Fls/`

| File | Role |
| --- | --- |
| `Fls/include/CGT.ARM.h` | Public header |
| `Fls/include/CGT.CCS.h` | Public header |
| `Fls/include/CGT.GHS.h` | Public header |
| `Fls/include/CGT.IAR.h` | Public header |
| `Fls/include/CGT.gcc.h` | Public header |
| `Fls/include/Compatibility.h` | Public header |
| `Fls/include/Constants.h` | Public header |
| `Fls/include/F021.h` | Public header |
| `Fls/include/FapiFunctions.h` | Public header |
| `Fls/include/Helpers.h` | Public header |
| `Fls/include/Registers.h` | Public header |
| `Fls/include/Registers_FMC_BE.h` | Public header |


_Showing a selection; the directory holds 0 C files and 14 headers in total._


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

Only standard AUTOSAR headers (`Std_Types.h`, Run-Time Environment headers) were observed.


## Configuration and usage

Configured through the driver's own configuration headers and the integration project's memory/linker layout. See the [Microcontroller Abstraction overview](./).
