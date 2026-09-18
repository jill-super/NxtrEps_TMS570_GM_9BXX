---
title: "Input Output Hardware Abstraction, User Part"
description: "Project signal access."
---
# Input Output Hardware Abstraction, User Part

:::note[Origin: Mixed origin — integration-owned]
This directory mixes in-house files, third-party files, and generated files. Each file header states its own owner; see the per-file notes below.
:::

## Purpose and responsibility

`GM_9BXX_EPS_TMS570/SwProject/IoHwAbstractionUsr/` (`IoHwAbstractionUsr.c/.h`) plus the shared `Source/IoHwAb.c` implement the project's Input/Output Hardware Abstraction: named signal-level access (discretes, analogs, PWM channels) for the Software Components, above the Vector Digital Input Output/Port/Analog drivers.

## Usage

Components access hardware only through these signals and the Run-Time Environment ports; pin mapping changes stay inside this abstraction and the Digital Input Output/Port configuration.
