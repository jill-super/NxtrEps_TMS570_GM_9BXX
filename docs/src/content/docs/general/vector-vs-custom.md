---
title: "Third-Party and Generated Code"
description: "How third-party and generated code are identified."
---
# Third-Party and Generated Code

Everything without an origin badge is in-house code (copyright headers name Nexteer Automotive). Only third-party and mixed origins are flagged with a badge. This page documents the rules that were applied by inspecting file copyright headers and generator stamps across the repository.

## Flagged origins

- **Vector-provided — MICROSAR Basic Software.** File headers carry `Copyright (c) ... Vector Informatik GmbH`. This covers the entire communication, memory, mode-management, diagnostic, and Operating System stack under the integration project's `SwProject/Source/BasicSoftware` folder, plus the generated Run-Time Environment, `GenData`, and Operating System configuration. Treat generated files as read-only: change behavior through DaVinci Configurator data and callbacks.
- **Third-party — Texas Instruments.** Headers carry Texas Instruments copyright. This covers the Flash EEPROM Emulation driver and the F021 Flash library. History entries show adaptations made at Vector's request during integration; prefer vendor updates over local edits.
- **Third-party — Gliwa GmbH.** Headers carry Gliwa copyright. This covers the T1 timing-measurement instrumentation only.
- **Mixed origin.** The integration project root and the standard-types package mix in-house, third-party, and generated files; each file header states its own owner.
- **No badge.** In-house code: Application Software components, sensor/actuator components, Complex Device Drivers, the Diagnostic Manager, the Common Diagnostic Services, the Measurement and Calibration Protocol wrapper, and the shared library. Note: many of these files also carry a `MICROSAR RTE Generator` stamp line. That stamp records which tool generated the Software Component interface scaffolding; the control logic itself is in-house, so no badge is shown.

## How to verify for any file

1. Open the file and read the copyright banner at the top.
2. `Vector Informatik` → Vector-provided. `Texas Instruments` → Texas Instruments third-party. `Gliwa` → Gliwa third-party. Anything else (normally `Nexteer`) → in-house, no badge.
3. `MICROSAR RTE Generator` / `DaVinci` / `GenData` stamps → generated interface or configuration; owned by whoever owns the generator input (in-house for Software Component templates, Vector for stack configuration).

## Practical consequences

- In-house code is reviewed, tested, and calibrated internally; start here when changing steering behavior.
- Vector-provided and Texas Instruments code should be upgraded by importing a new vendor release, never by hand-editing, except for the explicitly marked project callbacks and configuration files.
- Safety analysis must treat third-party components as Safety Elements out of Context with their own safety manuals.
