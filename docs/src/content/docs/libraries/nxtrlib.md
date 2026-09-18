---
title: "Shared Software Library (NxtrLib)"
description: "In-house shared library: digital filters, fixed-point math, interpolation, sine/cosine helpers, checksums, and system-time utilities used across Software Compon"
---

# Shared Software Library

Directory: `NxtrLib` · AUTOSAR group: Shared Libraries and Platform


## Purpose and responsibility

In-house shared library: digital filters, fixed-point math, interpolation, sine/cosine helpers, checksums, and system-time utilities used across Software Components.

## Source layout

Repository path: `NxtrLib/`

| File | Role |
| --- | --- |
| `NxtrLib/src/CheckSums.c` | Implementation |
| `NxtrLib/src/SystemTime.c` | Implementation |
| `NxtrLib/src/atan2_octants.c` | Implementation |
| `NxtrLib/src/filters.c` | Implementation |
| `NxtrLib/src/interpolation.c` | Implementation |
| `NxtrLib/include/CheckSums.h` | Public header |
| `NxtrLib/include/Filter_Types.h` | Public header |
| `NxtrLib/include/GlobalMacro.h` | Public header |
| `NxtrLib/include/SinCos.h` | Public header |
| `NxtrLib/include/SystemTime.h` | Public header |
| `NxtrLib/include/atan2.h` | Public header |
| `NxtrLib/include/filters.h` | Public header |
| `NxtrLib/include/fixmath.h` | Public header |
| `NxtrLib/include/fpmtype.h` | Public header |
| `NxtrLib/include/interpolation.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `CheckSums.h`
- `GlobalMacro.h`
- `Gpt.h`
- `Gpt_Cfg.h`
- `MemMap.h`
- `Rte_NexteerLibs.h`
- `SystemTime.h`
- `SystemTime_Cfg.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Consumed directly by other modules through its public headers. See the depending module pages for usage context.
