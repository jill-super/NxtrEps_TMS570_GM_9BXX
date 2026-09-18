---
title: "Timing Measurement and Tracing T1 (GliwaT1)"
description: "Third-party timing-analysis instrumentation by Gliwa GmbH (T1): target-specific hooks, runnable tracing, and metrics plumbing."
---

# Timing Measurement and Tracing T1

Directory: `GliwaT1` · AUTOSAR group: Shared Libraries and Platform

:::note[Origin: Third-party — Gliwa GmbH]
This module is third-party timing-analysis software supplied by Gliwa GmbH. Copyright headers name Gliwa GmbH.
:::

## Purpose and responsibility

Third-party timing-analysis instrumentation by Gliwa GmbH (T1): target-specific hooks, runnable tracing, and metrics plumbing.

## Source layout

Repository path: `GliwaT1/`

| File | Role |
| --- | --- |
| `GliwaT1/src/T1_AppInterface.c` | Implementation |
| `GliwaT1/src/T1_config.c` | Implementation |
| `GliwaT1/include/Metrics.h` | Public header |
| `GliwaT1/include/T1_AppInterface.h` | Public header |
| `GliwaT1/include/T1_MemMap.h` | Public header |
| `GliwaT1/include/T1_baseConfig.h` | Public header |
| `GliwaT1/include/T1_baseInterface.h` | Public header |
| `GliwaT1/include/T1_bid.h` | Public header |
| `GliwaT1/include/T1_config.h` | Public header |
| `GliwaT1/include/T1_contConfig.h` | Public header |
| `GliwaT1/include/T1_contInterface.h` | Public header |
| `GliwaT1/include/T1_delayConfig.h` | Public header |
| `GliwaT1/include/T1_delayInterface.h` | Public header |
| `GliwaT1/include/T1_flexConfig.h` | Public header |


_Showing a selection; the directory holds 2 C files and 19 headers in total._


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `T1_AppInit()`
- `T1_AppHandler()`
- `T1_AppBgHandler()`
- `osPrefetchAbort()`
- `osDataAbort()`


## Dependencies

- `T1_AppInterface.h`
- `T1_AppInterface_Cfg.h`
- `T1_MemMap.h`
- `T1_baseConfig.h`
- `T1_bid.h`
- `T1_contConfig.h`
- `T1_delayConfig.h`
- `T1_flexConfig.h`
- `T1_scopeConfig.h`
- `osek.h`


## Configuration and usage

Consumed directly by other modules through its public headers. See the depending module pages for usage context.
