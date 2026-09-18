---
title: "Standard Type Definitions and Platform Headers (StdDef)"
description: "AUTOSAR standard types (Std_Types, Platform_Types, Compiler abstraction) plus Texas Instruments compiler support headers. Mostly Texas Instruments and in-house "
---

# Standard Type Definitions and Platform Headers

Directory: `StdDef` · AUTOSAR group: Shared Libraries and Platform

:::note[Origin: Mixed origin — integration-owned]
This directory mixes in-house files, third-party files, and generated files. Each file header states its own owner; see the per-file notes below.
:::

## Purpose and responsibility

AUTOSAR standard types (Std_Types, Platform_Types, Compiler abstraction) plus Texas Instruments compiler support headers. Mostly Texas Instruments and in-house headers; a few Vector headers are present.

## Source layout

Repository path: `StdDef/`

| File | Role |
| --- | --- |
| `StdDef/include/Compiler.h` | Public header |
| `StdDef/include/Platform_Types.h` | Public header |
| `StdDef/include/Std_Types.h` | Public header |
| `StdDef/include/TMS570_4_9_1/include/_fmt_specifier.h` | Public header |
| `StdDef/include/TMS570_4_9_1/include/_isfuncdcl.h` | Public header |
| `StdDef/include/TMS570_4_9_1/include/_isfuncdef.h` | Public header |
| `StdDef/include/TMS570_4_9_1/include/_lock.h` | Public header |
| `StdDef/include/TMS570_4_9_1/include/access.h` | Public header |
| `StdDef/include/TMS570_4_9_1/include/assert.h` | Public header |
| `StdDef/include/TMS570_4_9_1/include/cpy_tbl.h` | Public header |
| `StdDef/include/TMS570_4_9_1/include/crc_tbl.h` | Public header |
| `StdDef/include/TMS570_4_9_1/include/ctype.h` | Public header |


_Showing a selection; the directory holds 0 C files and 120 headers in total._


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

Only standard AUTOSAR headers (`Std_Types.h`, Run-Time Environment headers) were observed.


## Configuration and usage

Consumed directly by other modules through its public headers. See the depending module pages for usage context.
