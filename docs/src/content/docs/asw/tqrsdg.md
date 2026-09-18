---
title: "Torque Residual Diagnostic, System Function 31 (TqRsDg)"
description: "Implements System Function SF31: residual-based torque plausibility diagnostic. Assumption: short name expands to torque-residual diagnostic; the source header "
---

# Torque Residual Diagnostic, System Function 31

Directory: `TqRsDg` · AUTOSAR group: Application Software


## Purpose and responsibility

Implements System Function SF31: residual-based torque plausibility diagnostic. Assumption: short name expands to torque-residual diagnostic; the source header is normative.

## Source layout

Repository path: `TqRsDg/`

| File | Role |
| --- | --- |
| `TqRsDg/src/Ap_TqRsDg.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_TqRsDg_Per1_MtrCurrIdptSig_Cnt_u08()`


## Dependencies

- `Ap_TqRsDg_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_TqRsDg.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
