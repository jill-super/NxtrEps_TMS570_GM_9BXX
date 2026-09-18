---
title: "Transport Protocol (Tp)"
description: "Vector Transport Protocol for segmented diagnostic communication."
---
# Transport Protocol

Directory: `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Tp/` · AUTOSAR group: Basic Software (Vector MICROSAR stack)

:::note[Origin: Vector-provided — MICROSAR Basic Software]
This module is third-party software supplied by Vector Informatik as part of the MICROSAR Basic Software stack (including DaVinci Configurator generated data where applicable). Do not edit generated files; change behavior through configuration and callbacks.
:::

## Purpose and responsibility

Vector Transport Protocol for segmented diagnostic communication.

## Source layout

Repository path: `GM_9BXX_EPS_TMS570/SwProject/Source/BSW/Tp/`

The directory carries the Vector implementation plus project-specific configuration siblings under `Source/GenData` (for example `*_Cfg.h`, `*_Lcfg.c`, `*_PBcfg.c` where applicable). Generated and configured files must be regenerated or edited through the configuration toolchain, not by hand where the file banner forbids it.

## Configuration and usage

Configured with the DaVinci Configurator data checked into `Source/GenData`, `Source/GenDataRte`, and `Source/GenDataOS`, and consumed by the in-house components through the Run-Time Environment and the ECU Abstraction interfaces. See the [Electronic Control Unit Integration Project](../../integration/gm_9bxx_eps_tms570/) and the [Run-Time Environment and Generated Code](../../integration/rte-and-generated-code/) pages.
