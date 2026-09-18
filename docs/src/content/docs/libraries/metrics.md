---
title: "Runtime Metrics Interface (Metrics)"
description: "Runtime metrics/data-logging interface feeding the tracing and measurement plumbing."
---

# Runtime Metrics Interface

Directory: `Metrics` · AUTOSAR group: Shared Libraries and Platform


## Purpose and responsibility

Runtime metrics/data-logging interface feeding the tracing and measurement plumbing.

## Source layout

Repository path: `Metrics/`

| File | Role |
| --- | --- |
| `Metrics/src/Metrics.c` | Implementation |
| `Metrics/include/Metrics.h` | Public header |
| `Metrics/include/Metrics_Enable.h` | Public header |
| `Metrics/include/sys_pmu.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Metrics_RunnableStart()`


## Dependencies

- `Det.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Metrics.h`
- `Metrics_Enable.h`
- `Rte_Type.h`
- `SystemTime.h`
- `filters.h`
- `oseksctx.h`
- `sys_pmu.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Consumed directly by other modules through its public headers. See the depending module pages for usage context.
