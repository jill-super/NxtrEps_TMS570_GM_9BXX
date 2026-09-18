---
title: "Electric Power Steering — Technical Documentation"
description: "AUTOSAR-based Electric Power Steering software documentation."
---
# Electric Power Steering — Technical Documentation

Complete reference for the AUTOSAR-based Electric Power Steering system on the Texas Instruments TMS570 microcontroller: layer organization, every software module, third-party versus in-house origin, and the build.

## Start here

- [Application Software (70 modules)](./asw/) — AUTOSAR Software Components implementing steering functions, sensing, arbitration, diagnostics, and protection.
- [Complex Device Drivers (13 modules)](./cdd/) — Complex Device Drivers: non-standardized drivers that access hardware directly where AUTOSAR specifies no module.
- [Basic Software (4 modules)](./bsw/) — Basic Software services and communication layers: in-house diagnostic services plus the Vector MICROSAR stack.
- [Microcontroller Abstraction (2 modules)](./mcal/) — Microcontroller Abstraction Layer: third-party Texas Instruments drivers for on-chip flash and emulation.
- [Electronic Control Unit Integration Project (2 modules)](./integration/) — The single buildable Electronic Control Unit project: integration code, generated code, configuration, and tooling.
- [Shared Libraries and Platform (4 modules)](./libraries/) — Shared code used across layers: standard types, math/filter library, tracing, and startup support.

- [AUTOSAR layer overview](./general/autosar-overview/) — how the layers fit together.
- [Third-party and generated code](./general/vector-vs-custom/) — how to recognize code that is not in-house.
- [Build system](./general/build-system/) — Code Composer Studio project, linker, and post-build tooling.
- [Document conversion log](./general/documentation-inventory/) — what happened to the Word and PDF documents.
- [Glossary](./general/glossary/) — every abbreviation expanded to its long name.

## Origin at a glance

All modules are in-house unless flagged otherwise. Vector-provided modules belong to the MICROSAR Basic Software stack by Vector Informatik, including DaVinci Configurator generated data. Texas Instruments modules cover the TMS570 Flash drivers, and the Gliwa T1 module covers timing instrumentation. The [third-party code guide](./general/vector-vs-custom/) explains the flagging rules.

## Module catalog

The catalog below uses long names everywhere for readability; the directory short name follows in parentheses.


### Application Software

- [Absolute Hardware Position over Inter-Integrated Circuit](./asw/abshwpos_tci2cvd/) (`AbsHwPos_TcI2cVd`)
- [Active Pull Compensation](./asw/activepull/) (`ActivePull`)
- [Analog Handwheel Torque Sensing](./asw/anahwtrq/) (`AnaHwTrq`)
- [Assist Output Firewall](./asw/assistfirewall/) (`AssistFirewall`)
- [Average Friction Learning](./asw/avgfriclrn/) (`AvgFricLrn`)
- [Base Power Assist Control](./asw/assist/) (`Assist`)
- [Battery Voltage Correlation Diagnostic](./asw/battvltgcorrln/) (`BattVltgCorrln`)
- [Battery Voltage Diagnostics](./asw/bvdiag/) (`BVDiag`)
- [Battery Voltage Measurement and Arbitration](./asw/battvltg/) (`BattVltg`)
- [Common Motor Current Measurement, Three-Phase Shunt](./asw/cmmtrcurr3phs/) (`CmMtrCurr3Phs`)
- [Component Error Handling](./asw/complerr/) (`ComplErr`)
- [Control Polarity for Brushless Control](./asw/ctrlpolaritybrshlss/) (`CtrlPolarityBrshlss`)
- [Controlled Velocity Return](./asw/ctrldvelrtn/) (`CtrldVelRtn`)
- [Controller Temperature Monitoring](./asw/ctrltemp/) (`CtrlTemp`)
- [Damping Output Firewall](./asw/dampingfirewall/) (`DampingFirewall`)
- [Digital Column Position Sensing](./asw/digcolps/) (`DigColPs`)
- [Digital Motor Position Sensor Arbitration](./asw/digmsbarbn/) (`DigMSBArbn`)
- [Electrical Power Management](./asw/elepwr/) (`ElePwr`)
- [End-of-Travel Actuator Management](./asw/eotactuatormng/) (`EOTActuatorMng`)
- [End-of-Travel Damping Firewall](./asw/etdmpfw/) (`EtDmpFw`)
- [End-of-Travel Learning](./asw/lrneot/) (`LrnEOT`)
- [Fault Injection Test Support](./asw/fltinjection/) (`FltInjection`)
- [Frequency Sweep Excitation](./asw/sweep/) (`Sweep`)
- [Frequency-Dependent Damping and Inertia Compensation](./asw/frqdepdmpninrtcmp/) (`FrqDepDmpnInrtCmp`)
- [General Position Trajectory Generation](./asw/genpostraj/) (`GenPosTraj`)
- [Hands-Off-Wheel Detection](./asw/howdetect/) (`HOWDetect`)
- [Handwheel Torque Arbitration](./asw/hwtrqarbn/) (`HwTrqArbn`)
- [Handwheel Torque Correlation Diagnostic](./asw/hwtqcorrln/) (`HwTqCorrln`)
- [Hardware Power-Up Sequencing](./asw/hwpwrupseq/) (`HwPwrUpSeq`)
- [High-Frequency Assist](./asw/highfreqassist/) (`HighFreqAssist`)
- [High-Load Stall Management](./asw/hiloadstall/) (`HiLoadStall`)
- [Hysteresis Compensation](./asw/hystcomp/) (`HystComp`)
- [Limit Coding](./asw/lmtcod/) (`LmtCod`)
- [Loss-of-Assist Management](./asw/loamgr/) (`LoaMgr`)
- [Motor Angle Correlation Diagnostic](./asw/motagcorrln/) (`MotAgCorrln`)
- [Motor Mechanical Position 1 Sensing](./asw/motmeclposn1/) (`MotMeclPosn1`)
- [Motor Mechanical Position 2 Sensing](./asw/motmeclposn2/) (`MotMeclPosn2`)
- [Motor Position Compensation](./asw/motposncmp/) (`MotPosnCmp`)
- [Motor Position from Triple Sine-Cosine Sensors](./asw/mtrpos3sincos/) (`MtrPos3SinCos`)
- [Motor Temperature Estimation](./asw/mtrtempest/) (`MtrTempEst`)
- [Motor Velocity from Digital Sensing](./asw/mtrvel_digi/) (`MtrVel_Digi`)
- [Over-Voltage Monitoring](./asw/ovrvoltmon/) (`OvrVoltMon`)
- [Position Servo Control](./asw/posservo/) (`PosServo`)
- [Power Disconnect for Dual Inverter](./asw/pwrdscntduinv/) (`PwrDscntDuInv`)
- [Power Limit Function Correction](./asw/pwrlmtfunccr/) (`PwrLmtFuncCr`)
- [Powerpack Service Data Recovery](./asw/gmpwrpksrvdatarcvry_cf034b/) (`GmPwrpkSrvDataRcvry_CF034B`)
- [Return Output Firewall](./asw/returnfirewall/) (`ReturnFirewall`)
- [Sensor Offset Correction](./asw/snsroffscorrn/) (`SnsrOffsCorrn`)
- [Sensor Offset Learning](./asw/snsroffslrng/) (`SnsrOffsLrng`)
- [Shutdown Mechanism](./asw/shtdnmech/) (`ShtdnMech`)
- [Signal Conditioning](./asw/sgnlcond/) (`SgnlCond`)
- [Sine Voltage Generation Diagnostics, Dual Inverter](./asw/svdiag_dualinv/) (`SVDiag_DualInv`)
- [Stability Compensation](./asw/stabilitycomp/) (`StabilityComp`)
- [Start-Stop Function](./asw/gmstrtstop/) (`GMStrtStop`)
- [State Output Control](./asw/stopctrl/) (`StOpCtrl`)
- [Steering Damping Control](./asw/damping/) (`Damping`)
- [System State Manager](./asw/stamd/) (`StaMd`)
- [Temporal Monitor for Dual Inverter](./asw/tmplmonrdualivtr/) (`TmplMonrDualIvtr`)
- [Thermal Duty Cycle Management](./asw/thrmdutycycle/) (`ThrmDutyCycle`)
- [Torque Arbitration Limit, Customer Feature 10](./asw/trqarblim/) (`TrqArblim`)
- [Torque Disturbance Mitigation, System Function 47](./asw/sf47_tsmit_implementation/) (`SF47_TSMit_Implementation`)
- [Torque Oscillation Control](./asw/trqosc/) (`TrqOsc`)
- [Torque Overlay State, Customer Feature 09](./asw/trqovlsta/) (`TrqOvlSta`)
- [Torque Path Loss-of-Assist Handling](./asw/trqloa/) (`TrqLOA`)
- [Torque Residual Diagnostic, System Function 31](./asw/tqrsdg/) (`TqRsDg`)
- [Translational Damping, legacy System Function 26](./asw/tranldampg/) (`TranlDampg`)
- [Tuning Selection Authorization](./asw/tuningselauth/) (`TuningSelAuth`)
- [Vehicle Dynamics Compensation](./asw/vehdyn/) (`VehDyn`)
- [Vehicle Speed Limiting Interface](./asw/vehspdlmt/) (`VehSpdLmt`)
- [Wheel Imbalance Rejection](./asw/whlimbrej/) (`WhlImbRej`)

### Complex Device Drivers

- [Analog-to-Digital Converter Driver](./cdd/adc/) (`Adc`)
- [Assist Limit, Current Mode](./cdd/astlmt_cm/) (`AstLmt_CM`)
- [Direct Memory Access Driver](./cdd/dma/) (`Dma`)
- [Enhanced Pulse-Width Modulation Setup](./cdd/epwm_up/) (`ePWM_Up`)
- [High-End Timer Module 1 Configuration and Use](./cdd/nhet1cfganduse/) (`Nhet1CfgAndUse`)
- [Inter-Integrated Circuit Driver](./cdd/i2cnxtr/) (`I2cNxtr`)
- [Microcontroller Diagnostics](./cdd/tms570_udiag/) (`TMS570_uDiag`)
- [Motor Control, Current Mode](./cdd/mtrctrl_cm/) (`MtrCtrl_CM`)
- [Motor Phase Feedback Measurement](./cdd/phasefdbkmeas/) (`PhaseFdbkMeas`)
- [Non-Volatile Memory Manager](./cdd/nvmmgr/) (`NvMMgr`)
- [Non-Volatile Memory Proxy](./cdd/nvmproxy/) (`NvMProxy`)
- [Serial Peripheral Interface Driver](./cdd/spinxt/) (`SpiNxt`)
- [Space-Vector Driver, Current Mode](./cdd/svdrvr_cm/) (`SVDrvr_CM`)

### Basic Software

- [Common Diagnostic Services, Shared Implementation](./bsw/cms_common/) (`CMS_Common`)
- [Diagnostic Manager](./bsw/diagmgr/) (`DiagMgr`)
- [Measurement and Calibration Protocol Wrapper](./bsw/xcp/) (`Xcp`)
- [Serial Communication Output Service](./bsw/gmsrlcomoutput/) (`GMSrlComOutput`)

### Microcontroller Abstraction

- [Flash EEPROM Emulation Driver](./mcal/fee/) (`Fee`)
- [Flash Memory Driver](./mcal/fls/) (`Fls`)

### Electronic Control Unit Integration Project

- [Microcontroller Startup and Core Initialization](./integration/tms570_startup/) (`TMS570_Startup`)
- [Vehicle Integration Project for the Target Platform](./integration/gm_9bxx_eps_tms570/) (`GM_9BXX_EPS_TMS570`)

### Shared Libraries and Platform

- [Runtime Metrics Interface](./libraries/metrics/) (`Metrics`)
- [Shared Software Library](./libraries/nxtrlib/) (`NxtrLib`)
- [Standard Type Definitions and Platform Headers](./libraries/stddef/) (`StdDef`)
- [Timing Measurement and Tracing T1](./libraries/gliwat1/) (`GliwaT1`)
