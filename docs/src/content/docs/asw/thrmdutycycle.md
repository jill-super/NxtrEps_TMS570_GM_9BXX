---
title: "Thermal Duty Cycle Management (ThrmDutyCycle)"
description: "Limits duty cycle based on thermal models to protect motor and electronics (Software Component Ap_ThrmlDutyCycle)."
---

# Thermal Duty Cycle Management

Directory: `ThrmDutyCycle` · AUTOSAR group: Application Software


## Purpose and responsibility

Limits duty cycle based on thermal models to protect motor and electronics (Software Component Ap_ThrmlDutyCycle).

## Source layout

Repository path: `ThrmDutyCycle/`

| File | Role |
| --- | --- |
| `ThrmDutyCycle/src/Ap_ThrmlDutyCycle.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_ThrmlDutyCycle_Per1_DutyCycleLevel_Uls_f32()`
- `Rte_IWrite_ThrmlDutyCycle_Per1_ThermLimitPerc_Uls_f32()`
- `Rte_IWrite_ThrmlDutyCycle_Per1_ThermalLimit_MtrNm_f32()`


## Dependencies

- `Ap_ThrmlDutyCycle_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_ThrmlDutyCycle.h`
- `filters.h`
- `fixmath.h`
- `interpolation.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
