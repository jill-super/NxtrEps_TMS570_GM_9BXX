---
title: "Common Diagnostic Services, Shared Implementation (CMS_Common)"
description: "Shared implementation of the Common Manufacturing/Diagnostic Services for International Organization for Standardization (UDS/ISO) and Universal Measurement and"
---

# Common Diagnostic Services, Shared Implementation

Directory: `CMS_Common` · AUTOSAR group: Basic Software


## Purpose and responsibility

Shared implementation of the Common Manufacturing/Diagnostic Services for International Organization for Standardization (UDS/ISO) and Universal Measurement and Calibration Protocol (XCP) service handling. Assumption: CMS expands to Common Manufacturing Services per the EPS_DiagSrvcs file naming; stated where used.

## Source layout

Repository path: `CMS_Common/`

| File | Role |
| --- | --- |
| `CMS_Common/src/EPS_DiagSrvcs_ISO.c` | Implementation |
| `CMS_Common/src/EPS_DiagSrvcs_XCP.Vector.c` | Implementation |
| `CMS_Common/src/EPS_DiagSrvcs_XCP.c` | Implementation |
| `CMS_Common/include/EPS_DiagSrvcs_CommonData.h` | Public header |
| `CMS_Common/include/EPS_DiagSrvcs_ISO.h` | Public header |
| `CMS_Common/include/EPS_DiagSrvcs_SrvcLUTbl.h` | Public header |
| `CMS_Common/include/EPS_DiagSrvcs_XCP.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `EPS_DiagSrvcs_CommonData.h`
- `EPS_DiagSrvcs_ISO.Interface.h`
- `EPS_DiagSrvcs_ISO.h`
- `EPS_DiagSrvcs_SrvcLUTbl.h`
- `EPS_DiagSrvcs_XCP.Interface.h`
- `EPS_DiagSrvcs_XCP.h`
- `MemMap.h`
- `SystemTime.h`
- `tiotp_regs.h`


## Configuration and usage

Configured through DaVinci Configurator data in the integration project (`Source/GenData`) and project-specific callbacks. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/).
