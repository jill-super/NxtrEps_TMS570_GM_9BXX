---
title: "Serial Communication Output Service (GMSrlComOutput)"
description: "Basic-Software-side serial communication output service used by the application output stage. Listed under Basic Software because it serves as a communication s"
---

# Serial Communication Output Service

Directory: `GMSrlComOutput` · AUTOSAR group: Basic Software


## Purpose and responsibility

Basic-Software-side serial communication output service used by the application output stage. Listed under Basic Software because it serves as a communication service; the application stage lives with the Application Software layer.

## Source layout

Repository path: `GMSrlComOutput/`

| File | Role |
| --- | --- |
| `GMSrlComOutput/src/Ap_SrlComOutput.c` | Implementation |
| `GMSrlComOutput/include/Ap_SrlComOutput.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `Ap_DemIf.h`
- `Ap_DfltConfigData.h`
- `Ap_SrlComOutput.h`
- `Ap_SrlComOutput_Cfg.h`
- `CDD_Data.h`
- `CalConstants.h`
- `Dem.h`
- `Dem_Lcfg.h`
- `DiagMgr_Cfg.h`
- `GlobalMacro.h`


## Configuration and usage

Configured through DaVinci Configurator data in the integration project (`Source/GenData`) and project-specific callbacks. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/).
