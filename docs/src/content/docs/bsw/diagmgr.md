---
title: "Diagnostic Manager (DiagMgr)"
description: "Core Diagnostic Manager: debounces Network Trouble Codes, interfaces the AUTOSAR Diagnostic Event Manager, and computes fault-response/latch actions (dual-inver"
---

# Diagnostic Manager

Directory: `DiagMgr` · AUTOSAR group: Basic Software


## Purpose and responsibility

Core Diagnostic Manager: debounces Network Trouble Codes, interfaces the AUTOSAR Diagnostic Event Manager, and computes fault-response/latch actions (dual-inverter aware).

## Source layout

Repository path: `DiagMgr/`

| File | Role |
| --- | --- |
| `DiagMgr/src/Ap_DiagMgr_Core.c` | Implementation |
| `DiagMgr/src/Ap_DiagMgr_DemIf.c` | Implementation |
| `DiagMgr/src/Ap_DiagMgr_FailAction.c` | Implementation |
| `DiagMgr/include/Ap_DiagMgr.h` | Public header |
| `DiagMgr/include/Ap_DiagMgr_Types.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `Ap_DiagMgr.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `NvM.h`
- `Os.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured through DaVinci Configurator data in the integration project (`Source/GenData`) and project-specific callbacks. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/).
