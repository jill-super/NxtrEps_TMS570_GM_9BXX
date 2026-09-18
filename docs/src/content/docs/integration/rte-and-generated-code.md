---
title: "Run-Time Environment and Generated Code"
description: "GenData, RTE, OS configuration."
---
# Run-Time Environment and Generated Code

:::note[Origin: Mixed origin — integration-owned]
This directory mixes in-house files, third-party files, and generated files. Each file header states its own owner; see the per-file notes below.
:::

## What is generated

| Location (repository-relative) | Content | Owner |
| --- | --- | --- |
| `GM_9BXX_EPS_TMS570/SwProject/Source/GenData/` | Per-component configuration (`Ap_*_Cfg.h`, `Dem_Cfg`, `NvM` data, `CalConstants`) | Mixed: Vector generator output with in-house component data |
| `GM_9BXX_EPS_TMS570/SwProject/Source/GenDataRte/` | Run-Time Environment: `Rte_Type.h` and per-component `Rte_<Component>.h` contracts | Vector MICROSAR Run-Time Environment Generator output |
| `GM_9BXX_EPS_TMS570/SwProject/Source/GenDataOS/` | Operating System configuration (tasks, alarms, resources) | Vector generator output |
| `GM_9BXX_EPS_TMS570/SwProject/Source/SchM.c`, `EcuM_Callout_Stubs.c`, `RteErrata*.c` | Scheduler, state-manager stubs, generator errata workarounds | In-house integration |

## Rules

- Never hand-edit files inside `GenDataRte` and `GenDataOS`; regenerate them.
- `RteErrata*.c` files document known generator issues and their in-house workarounds — read them before touching startup or mode logic.
- Component configuration headers (`Ap_*_Cfg.h`) are the primary tuning surface for Application Software behavior alongside calibration.
