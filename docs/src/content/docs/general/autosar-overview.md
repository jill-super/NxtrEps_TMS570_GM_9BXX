---
title: "AUTOSAR Layer Overview"
description: "How the software maps onto AUTOSAR layers."
---
# AUTOSAR Layer Overview

The software follows the AUTOSAR (Automotive Open System Architecture) layered model on a single Electronic Control Unit built around the Texas Instruments TMS570 microcontroller.

## Layer map

| AUTOSAR layer | Documentation group | What lives there |
| --- | --- | --- |
| Application Software | [Application Software](../asw/) | Steering functions as AUTOSAR Software Components (`Ap_*` application logic, `Sa_*` sensor/actuator logic): assist, damping, return, arbitration, correlation diagnostics, learning, and protection. |
| Complex Device Drivers | [Complex Device Drivers](../cdd/) | Non-standardized drivers with direct hardware access: Analog-to-Digital Converter, Direct Memory Access, Serial Peripheral Interface, Inter-Integrated Circuit, High-End Timer, phase feedback, motor control and driver stages, and microcontroller micro-diagnostics. |
| Basic Software — Services and ECU Abstraction | [Basic Software](../bsw/) | In-house services (Diagnostic Manager, Common Diagnostic Services, Measurement and Calibration Protocol wrapper, serial output) on top of the Vector MICROSAR stack (Communication Manager, Diagnostic Event Manager, Non-Volatile Memory Manager, Operating System, Watchdog Manager, and more). |
| Basic Software — Microcontroller Abstraction | [Microcontroller Abstraction](../mcal/) | Third-party Texas Instruments drivers: Flash EEPROM Emulation and the F021 Flash Application Programming Interface. |
| Run-Time Environment and integration | [Electronic Control Unit Integration Project](../integration/) | The single buildable project: integration-specific components, generated Run-Time Environment and Operating System data, calibration constants, linker layout, and post-build tooling. |
| Libraries and platform | [Shared Libraries and Platform](../libraries/) | Standard types, shared math/filter library, timing instrumentation, metrics, and startup code used across layers. |

## Data flow (simplified)

Sensors (handwheel torque, column/motor position, vehicle speed, battery voltage) are acquired through sensor Software Components and Complex Device Drivers, conditioned and arbitrated in Application Software, fused into assist/return/damping commands, plausibility-checked by firewall components, and actuated through the motor-control and driver stages. The Diagnostic Manager observes Network Trouble Codes throughout and talks to the AUTOSAR Diagnostic Event Manager; the State Manager owns the global state machine; Non-Volatile Memory services persist learned values and offsets.
