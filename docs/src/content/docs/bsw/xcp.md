---
title: "Measurement and Calibration Protocol Wrapper (Xcp)"
description: "Application Software Component Ap_ApXcp: thin in-house wrapper and callback layer over the Vector Universal Measurement and Calibration Protocol stack (data acq"
---

# Measurement and Calibration Protocol Wrapper

Directory: `Xcp` · AUTOSAR group: Basic Software


## Purpose and responsibility

Application Software Component Ap_ApXcp: thin in-house wrapper and callback layer over the Vector Universal Measurement and Calibration Protocol stack (data acquisition lists, tune-on-the-fly support).

## Source layout

Repository path: `Xcp/`

| File | Role |
| --- | --- |
| `Xcp/src/Ap_ApXcp.c` | Implementation |
| `Xcp/include/Ap_ApXcp.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_ApXcp_Per1_ActiveTunOvrPtrAddr_Cnt_u32()`
- `Rte_IWrite_ApXcp_Per1_TuningSessionActPtr_Cnt_u8()`


## Dependencies

- `Ap_ApXcp.h`
- `EPS_DiagSrvcs_SrvcLUTbl.h`
- `EPS_DiagSrvcs_XCP.Interface.h`
- `EPS_DiagSrvcs_XCP.h`
- `Eep_30_At25128.h`
- `Mcu.h`
- `MemMap.h`
- `Rte_Ap_ApXcp.h`
- `SystemTime.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured through DaVinci Configurator data in the integration project (`Source/GenData`) and project-specific callbacks. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/).
