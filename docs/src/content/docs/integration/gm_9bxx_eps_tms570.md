---
title: "Vehicle Integration Project for the Target Platform (GM_9BXX_EPS_TMS570)"
description: "Buildable ECU project: integration code, Vector stack, generated RTE/OS, calibration, tooling."
---

# Vehicle Integration Project for the Target Platform

Directory: `GM_9BXX_EPS_TMS570/` · AUTOSAR group: Electronic Control Unit Integration Project

:::note[Origin: Mixed origin — integration-owned]
This directory mixes in-house files, third-party files, and generated files. Each file header states its own owner; see the per-file notes below.
:::

## Purpose and responsibility

The single buildable Electronic Control Unit project for the target vehicle platform on the TMS570 microcontroller. It combines integration-specific Software Components, the Vector MICROSAR Basic Software stack, generated Run-Time Environment and Operating System data, calibration constants, the Code Composer Studio project definition, the linker command file, and the post-build tooling. See the [Build System](../general/build-system/) page for how it builds.

## Source layout

Repository path: `GM_9BXX_EPS_TMS570/SwProject/`

| File | Role |
| --- | --- |
| `GM_9BXX_EPS_TMS570/SwProject/CDDInterface/src/Sa_CDDInterface.c` | Complex Device Driver interface component — see [page](./cdd-interface/) |
| `GM_9BXX_EPS_TMS570/SwProject/CMS_9Bxx/` | Customer diagnostic services — see [page](./customer-diagnostics/) |
| `GM_9BXX_EPS_TMS570/SwProject/IoHwAbstractionUsr/` | User hardware abstraction — see [page](./io-hardware-abstraction/) |
| `GM_9BXX_EPS_TMS570/SwProject/Source/GenData/` | Generated component configuration — see [page](./rte-and-generated-code/) |
| `GM_9BXX_EPS_TMS570/SwProject/Source/GenDataRte/` | Generated Run-Time Environment — see [page](./rte-and-generated-code/) |
| `GM_9BXX_EPS_TMS570/SwProject/Source/GenDataOS/` | Generated Operating System configuration — see [page](./rte-and-generated-code/) |
| `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/` | Vector MICROSAR stack — see [Basic Software](../bsw/) and [Stack](../bsw/stack/) |
| `GM_9BXX_EPS_TMS570/SwProject/TMS570LS202x6SFlashLnk.cmd` | Linker command file — see [page](./build-link-and-postbuild/) |
| `GM_9BXX_EPS_TMS570/SwProject/postbuild.bat` | Post-build script — see [page](./build-link-and-postbuild/) |


## Integration sub-pages

- [Run-Time Environment and Generated Code](./rte-and-generated-code/)
- [Calibration Data](./calibration-data/)
- [Complex Device Driver Interface Component](./cdd-interface/)
- [Customer Diagnostic Services](./customer-diagnostics/)
- [Input Output Hardware Abstraction, User Part](./io-hardware-abstraction/)
- [Vehicle Integration Components](./vehicle-integration-components/)
- [Linker Layout and Post-Build Tooling](./build-link-and-postbuild/)


## Vehicle integration components

Checkpoint reporters, serial input, input qualification, customer services, plausibility diagnostics, speed arbitration, and power-mode handling are inventoried on the [Vehicle Integration Components](./vehicle-integration-components/) page.


## Notes and assumptions

The `BSW` stack directories are Vector-provided; the `SwProject` component directories, `CMS_9Bxx`, and `CDDInterface` are in-house; `GenData*` is generator output. Directory totals: 110 C files and 400 headers.
