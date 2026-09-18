---
title: "Calibration Data"
description: "Default calibration constants."
---
# Calibration Data

:::note[Origin: Mixed origin — integration-owned]
This directory mixes in-house files, third-party files, and generated files. Each file header states its own owner; see the per-file notes below.
:::

## Content

| Location | Content |
| --- | --- |
| `GM_9BXX_EPS_TMS570/SwProject/Source/GenData/CalConstants.c`, `CalConstants.h` | Default calibration constants for the Application Software components |
| `GM_9BXX_EPS_TMS570/SwProject/DfltConfigData/` (`Ap_DfltConfigData.c/.h`) | Default configuration dataset component |

Calibration values are tuned per vehicle variant with the Measurement and Calibration Protocol tooling (see the [Measurement and Calibration Protocol Wrapper](../bsw/xcp/)); the checked-in files are the defaults linked into the image.
