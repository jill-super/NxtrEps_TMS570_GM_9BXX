---
title: "Complex Device Driver Interface Component"
description: "Sa_CDDInterface bridge."
---
# Complex Device Driver Interface Component


## Purpose and responsibility

`GM_9BXX_EPS_TMS570/SwProject/CDDInterface/src/Sa_CDDInterface.c` implements the sensor/actuator component that bridges Application Software Components and the Complex Device Drivers, isolating hardware specifics behind a stable component interface.

## Usage

Application components call this interface instead of touching drivers directly; driver replacements therefore stay local to this component and the underlying Complex Device Drivers.
