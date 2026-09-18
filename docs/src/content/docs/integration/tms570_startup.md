---
title: "Microcontroller Startup and Core Initialization (TMS570_Startup)"
description: "Startup code, core init, reset handling."
---
# Microcontroller Startup and Core Initialization

Directory: `TMS570_Startup/` · AUTOSAR group: Electronic Control Unit Integration Project (startup support)

## Purpose and responsibility

Application and boot startup sequence for the TMS570: core initialization, memory setup, reset-cause handling, and silicon errata workarounds (SSWF021_45), plus startup self-test hooks.

## Source layout

Repository path: `TMS570_Startup/`

| File | Role |
| --- | --- |
| `TMS570_Startup/src/AppStartup.c` | Implementation |
| `TMS570_Startup/src/BootStartup.c` | Implementation |
| `TMS570_Startup/src/ResetCause.c` | Implementation |
| `TMS570_Startup/src/errata_SSWF021_45.c` | Implementation |
| `TMS570_Startup/src/prooftestv02.c` | Implementation |
| `TMS570_Startup/src/sys_startup.c` | Implementation |
| `TMS570_Startup/include/ResetCause.h` | Public header |
| `TMS570_Startup/include/errata_SSWF021_45.h` | Public header |
| `TMS570_Startup/include/errata_SSWF021_45_defs.h` | Public header |
| `TMS570_Startup/include/prooftestv02.h` | Public header |
| `TMS570_Startup/include/sys_core.h` | Public header |
| `TMS570_Startup/include/sys_memory.h` | Public header |
| `TMS570_Startup/include/sys_pmu.h` | Public header |

## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `BootStartup()`
- `Startup()`
- `DiagFailedReset()`
- `resetStartup()`
- `pwronStartup()`
- `afterSTC()`
- `setupPLL()`
- `trimLPO()`
- `setupFlash()`
- `periphInit()`

## Dependencies

- `Compiler.h`
- `MemMap.h`
- `Platform_Types.h`
- `ResetCause.h`
- `adc_regs.h`
- `appinit_cfg.h`
- `ccm_regs.h`
- `dcan_regs.h`
- `dma_regs.h`
- `efc_regs.h`

## Configuration and usage

Linked first into the image via the linker command file; runs before the Operating System and the Electronic Control Unit State Manager. See the [Linker Layout and Post-Build Tooling](./build-link-and-postbuild/) page.
