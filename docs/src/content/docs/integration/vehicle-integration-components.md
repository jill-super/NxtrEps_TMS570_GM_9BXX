---
title: "Vehicle Integration Components"
description: "ChkPtAp, inputs, power, speed."
---
# Vehicle Integration Components


## Purpose and responsibility

Small integration-owned Application Software Components that adapt the reusable steering functions to this vehicle line:

| Component directory | Responsibility |
| --- | --- |
| `ChkPtAp/` (`Ap_ChkPtAp8/9/10.c`) | Watchdog Manager checkpoint components reporting alive status per core/partition |
| `SrlComInput/` (`Ap_SrlComInput.c`) | Serial communication input conditioning |
| `WIRInputQual/` (`Ap_WIRInputQual.c`) | Wheel-rotation/analog input qualification (project-specific input path) |
| `CustPerSrvcs/` (`Ap_CustPerSrvcs.c`) | Customer periodic services |
| `SASPlausDiag/` (`Ap_SASPlausDiag.c`) | Steering-angle-sensor plausibility diagnostics |
| `DemIf/` | Project Diagnostic Event Manager interface glue |
| `VehSpdArbn/` | Vehicle-speed arbitration for this bus layout |
| `VehPwrMd/` | Vehicle power-mode handling |
| `DfltConfigData/` | Default configuration dataset (see [Calibration Data](./calibration-data/)) |
| `Header/` | Shared integration headers: scheduler, демон? — scheduler (`SchM_*`), interrupt, memory, and configuration headers |

## Usage

These components are configured like any Application Software Component through `Source/GenData` and calibrated through the shared calibration constants.
