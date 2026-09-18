---
title: "Hardware Power-Up Sequencing (HwPwrUpSeq)"
description: "Orders hardware and software initialization at power-up (functional description document 13C, legacy of ES013B)."
---

# Hardware Power-Up Sequencing

Directory: `HwPwrUpSeq` · AUTOSAR group: Application Software


## Purpose and responsibility

Orders hardware and software initialization at power-up (functional description document 13C, legacy of ES013B).

## Source layout

Repository path: `HwPwrUpSeq/`

| File | Role |
| --- | --- |
| `HwPwrUpSeq/src/Ap_HwPwrUpSeq.c` | Implementation |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_HwPwrUpSeq_Per1_MtrDrvr0InitStart_Cnt_lgc()`
- `Rte_IWrite_HwPwrUpSeq_Per1_MtrDrvr1InitStart_Cnt_lgc()`
- `Rte_IWrite_HwPwrUpSeq_Per1_OverVltgMonStart_Cnt_lgc()`
- `Rte_IWrite_HwPwrUpSeq_Per1_PwrDiscATestStart_Cnt_lgc()`
- `Rte_IWrite_HwPwrUpSeq_Per1_PwrDiscBTestStart_Cnt_lgc()`
- `Rte_IWrite_HwPwrUpSeq_Per1_TMFTestStart_Cnt_lgc()`


## Dependencies

- `MemMap.h`
- `Rte_Ap_HwPwrUpSeq.h`

Run-Time Environment (`Rte_*`) and Mode Management headers appear where the component is an AUTOSAR Software Component.


## Configuration and usage

Configured per Software Component through the integration project's generated configuration (`Source/GenData`, `Source/GenDataRte`) and the shared calibration constants. See the [Electronic Control Unit Integration Project](../integration/gm_9bxx_eps_tms570/) and the [Build System](../general/build-system/) pages.
