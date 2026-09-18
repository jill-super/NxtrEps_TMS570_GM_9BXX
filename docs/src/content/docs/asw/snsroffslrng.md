---
title: "Sensor Offset Learning (SnsrOffsLrng)"
description: "Learns sensor offsets online for use by the offset correction function."
---

# Sensor Offset Learning

Directory: `SnsrOffsLrng` · AUTOSAR group: Application Software


## Purpose and responsibility

Learns sensor offsets online for use by the offset correction function.

## Source layout

Repository path: `SnsrOffsLrng/`

| File | Role |
| --- | --- |
| `SnsrOffsLrng/src/Ap_SnsrOffsLrng.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_SnsrOffsLrng_Init1_HwAgOffs_HwDeg_f32()`
- `Rte_IWrite_SnsrOffsLrng_Init1_HwTqOffs_HwNm_f32()`
- `Rte_IWrite_SnsrOffsLrng_Init1_VehYawRateOffs_DegpS_f32()`
- `SnsrOffsLrng_ReadHwAgOffs()`
- `SnsrOffsLrng_ReadHwTqOffs()`
- `SnsrOffsLrng_ReadYawRateOffs()`
- `SnsrOffsLrng_RstHwTq()`
- `SnsrOffsLrng_RstYawAndAg()`
- `SnsrOffsLrng_SetHwAgOffs()`
- `SnsrOffsLrng_SetHwTqOffs()`


## Dependencies

- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Rte_Ap_SnsrOffsLrng.h`
- `filters.h`
- `fixmath.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
