# Electric Power Steering System

![License](https://img.shields.io/badge/License-MIT-green.svg)
![Language](https://img.shields.io/badge/Language-C-blue.svg)
![Standard](https://img.shields.io/badge/Standard-AUTOSAR-orange.svg)
![Microcontroller](https://img.shields.io/badge/MCU-TMS570-red.svg)
![Safety](https://img.shields.io/badge/Safety-ASIL_D-critical.svg)

Complete **Electric Power Steering** system software for the target vehicle platform, built on **AUTOSAR (Automotive Open System Architecture)** for the **Texas Instruments TMS570** microcontroller (Hercules family, Cortex-R4), developed to **ISO 26262 ASIL D (Automotive Safety Integrity Level D)** processes.

> **Documentation site:** the full reference lives in [`docs/`](docs/). See [Documentation](#documentation) below.

## Table of contents

- [Features](#features)
- [Repository structure](#repository-structure)
- [Module catalog](#module-catalog)
- [Installation and build](#installation-and-build)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Key components**
  - **TMS570 microcontroller**: Texas Instruments Hercules Cortex-R4 device that runs the steering control.
  - **AUTOSAR software architecture**: Application Software components, Complex Device Drivers, Run-Time Environment, and MICROSAR Basic Software.
  - **Functional safety to ASIL D**: redundant sensing, correlation diagnostics, firewalls, temporal monitoring, and a central Diagnostic Manager.
  - **Controller Area Network communication** with transport protocol, interaction layer, and network management.
  - **Unified Diagnostic Services and Measurement and Calibration Protocol** services for manufacturing, service, and calibration.
- **Functionality**
  - Precise power-assisted steering control with damping, return, friction/hysteresis compensation, and vibration rejection.
  - Electric motor power management: current-mode control, space-vector drive, thermal/voltage derating, and dual-inverter supervision.

## Repository structure

Each top-level folder is one software module (long names are used throughout this readme; the directory short name is in parentheses). The documentation site groups them by AUTOSAR layer.

<details>
<summary><strong>Application Software</strong> — steering functions as AUTOSAR Software Components</summary>

Application logic (`Ap_` prefix) and sensor/actuator logic (`Sa_` prefix): assist, damping, return, arbitration, correlation diagnostics, learning, state management, and protection. Full reference: [`docs/src/content/docs/asw/`](docs/src/content/docs/asw/).

</details>

<details>
<summary><strong>Complex Device Drivers</strong> — direct hardware access where AUTOSAR specifies no module</summary>

Analog-to-Digital Converter (`Adc`), Direct Memory Access (`Dma`), Serial Peripheral Interface (`SpiNxt`), Inter-Integrated Circuit (`I2cNxtr`), High-End Timer (`Nhet1CfgAndUse`), phase feedback (`PhaseFdbkMeas`), motor control and space-vector drive (`MtrCtrl_CM`, `SVDrvr_CM`, `AstLmt_CM`, `ePWM_Up`), Non-Volatile Memory helpers (`NvMMgr`, `NvMProxy`), and microcontroller diagnostics (`TMS570_uDiag`). Full reference: [`docs/src/content/docs/cdd/`](docs/src/content/docs/cdd/).

</details>

<details>
<summary><strong>Basic Software</strong> — services plus the Vector MICROSAR stack</summary>

In-house services: Diagnostic Manager (`DiagMgr`), Common Diagnostic Services (`CMS_Common`), Measurement and Calibration Protocol wrapper (`Xcp`), Serial Communication Output Service (`GMSrlComOutput`). Third-party Vector MICROSAR stack under the integration project (`GM_9BXX_EPS_TMS570/SwProject/Source/BSW/`): Controller Area Network driver, Communication Manager, Diagnostic Event Manager, Operating System, Non-Volatile Memory Manager, Watchdog Manager, and more. Full reference: [`docs/src/content/docs/bsw/`](docs/src/content/docs/bsw/).

</details>

<details>
<summary><strong>Microcontroller Abstraction</strong> — Texas Instruments third-party drivers</summary>

Flash EEPROM Emulation (`Fee`) and Flash memory driver (`Fls`). Full reference: [`docs/src/content/docs/mcal/`](docs/src/content/docs/mcal/).

</details>

<details>
<summary><strong>Electronic Control Unit Integration Project</strong> — the single buildable project</summary>

`GM_9BXX_EPS_TMS570/SwProject/`: integration components, Vector generated code (`GenData`, Run-Time Environment, Operating System data), calibration constants, Code Composer Studio project files, linker command file, and post-build tooling. Full reference: [`docs/src/content/docs/integration/`](docs/src/content/docs/integration/).

</details>

<details>
<summary><strong>Shared Libraries and Platform</strong> — code shared across layers</summary>

Standard type definitions (`StdDef`), shared software library (`NxtrLib`), timing instrumentation (`GliwaT1`), runtime metrics (`Metrics`). Startup code lives in `TMS570_Startup` (documented with the integration project). Full reference: [`docs/src/content/docs/libraries/`](docs/src/content/docs/libraries/).

</details>

## Module catalog

Origin legend: unmarked modules (`—`) are in-house · **Vector-provided** = MICROSAR Basic Software (Vector Informatik) · **Texas Instruments** = third-party microcontroller software · **Gliwa** = third-party timing software · **Mixed** = integration-owned mix of in-house, third-party, and generated files. Per-module evidence is on each documentation page.

<details>
<summary><strong>Application Software</strong></summary>

| Module (long name) | Directory | Origin |
| --- | --- | --- |
| Absolute Hardware Position over Inter-Integrated Circuit | `AbsHwPos_TcI2cVd` | — |
| Active Pull Compensation | `ActivePull` | — |
| Analog Handwheel Torque Sensing | `AnaHwTrq` | — |
| Assist Output Firewall | `AssistFirewall` | — |
| Average Friction Learning | `AvgFricLrn` | — |
| Base Power Assist Control | `Assist` | — |
| Battery Voltage Correlation Diagnostic | `BattVltgCorrln` | — |
| Battery Voltage Diagnostics | `BVDiag` | — |
| Battery Voltage Measurement and Arbitration | `BattVltg` | — |
| Common Motor Current Measurement, Three-Phase Shunt | `CmMtrCurr3Phs` | — |
| Component Error Handling | `ComplErr` | — |
| Control Polarity for Brushless Control | `CtrlPolarityBrshlss` | — |
| Controlled Velocity Return | `CtrldVelRtn` | — |
| Controller Temperature Monitoring | `CtrlTemp` | — |
| Damping Output Firewall | `DampingFirewall` | — |
| Digital Column Position Sensing | `DigColPs` | — |
| Digital Motor Position Sensor Arbitration | `DigMSBArbn` | — |
| Electrical Power Management | `ElePwr` | — |
| End-of-Travel Actuator Management | `EOTActuatorMng` | — |
| End-of-Travel Damping Firewall | `EtDmpFw` | — |
| End-of-Travel Learning | `LrnEOT` | — |
| Fault Injection Test Support | `FltInjection` | — |
| Frequency Sweep Excitation | `Sweep` | — |
| Frequency-Dependent Damping and Inertia Compensation | `FrqDepDmpnInrtCmp` | — |
| General Position Trajectory Generation | `GenPosTraj` | — |
| Hands-Off-Wheel Detection | `HOWDetect` | — |
| Handwheel Torque Arbitration | `HwTrqArbn` | — |
| Handwheel Torque Correlation Diagnostic | `HwTqCorrln` | — |
| Hardware Power-Up Sequencing | `HwPwrUpSeq` | — |
| High-Frequency Assist | `HighFreqAssist` | — |
| High-Load Stall Management | `HiLoadStall` | — |
| Hysteresis Compensation | `HystComp` | — |
| Limit Coding | `LmtCod` | — |
| Loss-of-Assist Management | `LoaMgr` | — |
| Motor Angle Correlation Diagnostic | `MotAgCorrln` | — |
| Motor Mechanical Position 1 Sensing | `MotMeclPosn1` | — |
| Motor Mechanical Position 2 Sensing | `MotMeclPosn2` | — |
| Motor Position Compensation | `MotPosnCmp` | — |
| Motor Position from Triple Sine-Cosine Sensors | `MtrPos3SinCos` | — |
| Motor Temperature Estimation | `MtrTempEst` | — |
| Motor Velocity from Digital Sensing | `MtrVel_Digi` | — |
| Over-Voltage Monitoring | `OvrVoltMon` | — |
| Position Servo Control | `PosServo` | — |
| Power Disconnect for Dual Inverter | `PwrDscntDuInv` | — |
| Power Limit Function Correction | `PwrLmtFuncCr` | — |
| Powerpack Service Data Recovery | `GmPwrpkSrvDataRcvry_CF034B` | — |
| Return Output Firewall | `ReturnFirewall` | — |
| Sensor Offset Correction | `SnsrOffsCorrn` | — |
| Sensor Offset Learning | `SnsrOffsLrng` | — |
| Shutdown Mechanism | `ShtdnMech` | — |
| Signal Conditioning | `SgnlCond` | — |
| Sine Voltage Generation Diagnostics, Dual Inverter | `SVDiag_DualInv` | — |
| Stability Compensation | `StabilityComp` | — |
| Start-Stop Function | `GMStrtStop` | — |
| State Output Control | `StOpCtrl` | — |
| Steering Damping Control | `Damping` | — |
| System State Manager | `StaMd` | — |
| Temporal Monitor for Dual Inverter | `TmplMonrDualIvtr` | — |
| Thermal Duty Cycle Management | `ThrmDutyCycle` | — |
| Torque Arbitration Limit, Customer Feature 10 | `TrqArblim` | — |
| Torque Disturbance Mitigation, System Function 47 | `SF47_TSMit_Implementation` | — |
| Torque Oscillation Control | `TrqOsc` | — |
| Torque Overlay State, Customer Feature 09 | `TrqOvlSta` | — |
| Torque Path Loss-of-Assist Handling | `TrqLOA` | — |
| Torque Residual Diagnostic, System Function 31 | `TqRsDg` | — |
| Translational Damping, legacy System Function 26 | `TranlDampg` | — |
| Tuning Selection Authorization | `TuningSelAuth` | — |
| Vehicle Dynamics Compensation | `VehDyn` | — |
| Vehicle Speed Limiting Interface | `VehSpdLmt` | — |
| Wheel Imbalance Rejection | `WhlImbRej` | — |

</details>

<details>
<summary><strong>Complex Device Drivers</strong></summary>

| Module (long name) | Directory | Origin |
| --- | --- | --- |
| Analog-to-Digital Converter Driver | `Adc` | — |
| Assist Limit, Current Mode | `AstLmt_CM` | — |
| Direct Memory Access Driver | `Dma` | — |
| Enhanced Pulse-Width Modulation Setup | `ePWM_Up` | — |
| High-End Timer Module 1 Configuration and Use | `Nhet1CfgAndUse` | — |
| Inter-Integrated Circuit Driver | `I2cNxtr` | — |
| Microcontroller Diagnostics | `TMS570_uDiag` | — |
| Motor Control, Current Mode | `MtrCtrl_CM` | — |
| Motor Phase Feedback Measurement | `PhaseFdbkMeas` | — |
| Non-Volatile Memory Manager | `NvMMgr` | — |
| Non-Volatile Memory Proxy | `NvMProxy` | — |
| Serial Peripheral Interface Driver | `SpiNxt` | — |
| Space-Vector Driver, Current Mode | `SVDrvr_CM` | — |

</details>

<details>
<summary><strong>Basic Software services</strong></summary>

| Module (long name) | Directory | Origin |
| --- | --- | --- |
| Common Diagnostic Services, Shared Implementation | `CMS_Common` | — |
| Diagnostic Manager | `DiagMgr` | — |
| Measurement and Calibration Protocol Wrapper | `Xcp` | — |
| Serial Communication Output Service | `GMSrlComOutput` | — |

**Vector MICROSAR stack (third-party, under the integration project)**

| Module (long name) | Directory | Origin |
| --- | --- | --- |
| Communication Manager | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/ComM` | Vector-provided — MICROSAR Basic Software |
| Controller Area Network Driver | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Can` | Vector-provided — MICROSAR Basic Software |
| Cyclic Redundancy Check Library | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Crc` | Vector-provided — MICROSAR Basic Software |
| Default Error Tracer | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Det` | Vector-provided — MICROSAR Basic Software |
| Diagnostic Event Manager | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Dem` | Vector-provided — MICROSAR Basic Software |
| Diagnostic Gateway Glue | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Diag` | Vector-provided — MICROSAR Basic Software |
| Digital Input Output Driver | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Dio` | Vector-provided — MICROSAR Basic Software |
| Electronic Control Unit State Manager | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/EcuM` | Vector-provided — MICROSAR Basic Software |
| General Purpose Timer Driver | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Gpt` | Vector-provided — MICROSAR Basic Software |
| Input Output Hardware Abstraction | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/IoHwAb` | Vector-provided — MICROSAR Basic Software |
| Interaction Layer | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Il` | Vector-provided — MICROSAR Basic Software |
| Measurement and Calibration Protocol Stack | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Xcp` | Vector-provided — MICROSAR Basic Software |
| Memory Abstraction Interface | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/MemIf` | Vector-provided — MICROSAR Basic Software |
| Microcontroller Unit Driver | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Mcu` | Vector-provided — MICROSAR Basic Software |
| Network Management | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Nm` | Vector-provided — MICROSAR Basic Software |
| Non-Volatile Memory Manager | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/NvM` | Vector-provided — MICROSAR Basic Software |
| Operating System | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Os` | Vector-provided — MICROSAR Basic Software |
| Port Driver | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Port` | Vector-provided — MICROSAR Basic Software |
| Stack Common Headers | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/_Common` | Vector-provided — MICROSAR Basic Software |
| Transport Protocol | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Tp` | Vector-provided — MICROSAR Basic Software |
| Vector Standard Library | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/VStdLib` | Vector-provided — MICROSAR Basic Software |
| Watchdog Driver | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Wdg` | Vector-provided — MICROSAR Basic Software |
| Watchdog Interface | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/WdgIf` | Vector-provided — MICROSAR Basic Software |
| Watchdog Manager | `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/WdgM` | Vector-provided — MICROSAR Basic Software |

</details>

<details>
<summary><strong>Microcontroller Abstraction (Texas Instruments)</strong></summary>

| Module (long name) | Directory | Origin |
| --- | --- | --- |
| Flash EEPROM Emulation Driver | `Fee` | Third-party — Texas Instruments |
| Flash Memory Driver | `Fls` | Third-party — Texas Instruments |

</details>

<details>
<summary><strong>Integration project and shared platform</strong></summary>

| Module (long name) | Directory | Origin |
| --- | --- | --- |
| Microcontroller Startup and Core Initialization | `TMS570_Startup` | — |
| Vehicle Integration Project for the Target Platform | `GM_9BXX_EPS_TMS570` | Mixed origin — integration-owned |
| Runtime Metrics Interface | `Metrics` | — |
| Shared Software Library | `NxtrLib` | — |
| Standard Type Definitions and Platform Headers | `StdDef` | Mixed origin — integration-owned |
| Timing Measurement and Tracing T1 | `GliwaT1` | Third-party — Gliwa GmbH |

</details>

## Installation and build

No Makefiles or CMake files are used. The firmware builds with **Texas Instruments Code Composer Studio** (managed `gmake`). No workflow files exist in the repository, so there is no automated build to trigger — build locally as described below.

**Firmware (Windows host required for the production image)**

1. Install Texas Instruments Code Composer Studio with Hercules TMS570 code generation tools (the project targets Code Generation Tools 4.6.4).
2. Import `GM_9BXX_EPS_TMS570/SwProject` as an existing Code Composer Studio project (device `TMS570LS20216`, big-endian).
3. Build the `all` target from the IDE.
4. Run `SwProject/postbuild.bat` with the output base name to produce the flashable hex artifacts (checksum correction, `hex470`, memory accounting).
5. Flash the resulting image onto the TMS570 microcontroller with the Texas Instruments flashing tools.

Full detail: [Build System](docs/src/content/docs/general/build-system.md).

## Documentation

- Start at the documentation landing page: [`docs/src/content/docs/index.md`](docs/src/content/docs/index.md) — it links every AUTOSAR layer, every module page, and the general guides.
- [AUTOSAR layer overview](docs/src/content/docs/general/autosar-overview.md) · [Third-party and generated code](docs/src/content/docs/general/vector-vs-custom.md) · [Build system](docs/src/content/docs/general/build-system.md) · [Document conversion log](docs/src/content/docs/general/documentation-inventory.md) · [Glossary](docs/src/content/docs/general/glossary.md).
- Note on sources: the repository contains **no Word or PDF documents and no `doc/` folders** (verified by a case-insensitive tree search; see the conversion log), so module pages are written from the C sources, headers, and project files. Where a short name's expansion is an assumption, the page says so.
- Target vehicle platform: the software targets the General Motors 9BXX electrical architecture family (compact and mid-size sport-utility vehicles), integrated through the `GM_9BXX_EPS_TMS570` project.

## Contributing

We encourage contributions! If you'd like to improve this project, please submit a pull request. Keep generated and third-party files (Vector, Texas Instruments, Gliwa) untouched; change behavior through configuration, callbacks, and in-house modules.

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for the full text.
