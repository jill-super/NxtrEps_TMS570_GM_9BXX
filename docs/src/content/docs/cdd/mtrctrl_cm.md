---
title: "Motor Control, Current Mode (MtrCtrl_CM)"
description: "Generates the current command and voltage reference for current control, including Proportional-Integral current control. Assumption: suffix CM expands to Curre"
---

# Motor Control, Current Mode

Directory: `MtrCtrl_CM` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Generates the current command and voltage reference for current control, including Proportional-Integral current control. Assumption: suffix CM expands to Current Mode.

## Source layout

Repository path: `MtrCtrl_CM/`

| File | Role |
| --- | --- |
| `MtrCtrl_CM/src/Ap_CurrCmd.c` | Implementation |
| `MtrCtrl_CM/src/Ap_CurrParamComp.c` | Implementation |
| `MtrCtrl_CM/src/Ap_PICurrCntrl.c` | Implementation |
| `MtrCtrl_CM/src/Ap_PeakCurrEst.c` | Implementation |
| `MtrCtrl_CM/src/Ap_QuadDet.c` | Implementation |
| `MtrCtrl_CM/src/Ap_TrqCanc.c` | Implementation |
| `MtrCtrl_CM/src/Ap_TrqCmdScl.c` | Implementation |
| `MtrCtrl_CM/include/Ap_MtrCtrl.h` | Public header |


## Public interface

Representative symbols observed in the implementation (runnables, init, and helper functions; static helpers may be included):

- `Rte_IWrite_CurrParamComp_Init_EstKe_VpRadpS_f32()`
- `Rte_IWrite_CurrParamComp_Init_EstLd_Henry_f32()`
- `Rte_IWrite_CurrParamComp_Init_EstLq_Henry_f32()`
- `Rte_IWrite_CurrParamComp_Init_EstR_Ohm_f32()`
- `Rte_IWrite_CurrParamComp_Per1_EstKe_VpRadpS_f32()`
- `Rte_IWrite_CurrParamComp_Per1_EstLd_Henry_f32()`
- `Rte_IWrite_CurrParamComp_Per1_EstLq_Henry_f32()`
- `Rte_IWrite_CurrParamComp_Per1_EstR_Ohm_f32()`
- `SCom_EOLNomMtrParam_Get()`
- `SCom_EOLNomMtrParam_Set()`


## Dependencies

- `Ap_CurrCmd_Cfg.h`
- `Ap_CurrParamComp_Cfg.h`
- `Ap_MtrCtrl.h`
- `Ap_QuadDet_Cfg.h`
- `Ap_TrqCanc_Cfg.h`
- `Ap_TrqCmdScl_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `Interpolation.h`
- `MemMap.h`


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
