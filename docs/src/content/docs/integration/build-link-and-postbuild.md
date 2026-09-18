---
title: "Linker Layout and Post-Build Tooling"
description: "Command file and postbuild script."
---
# Linker Layout and Post-Build Tooling


## Linker command file

`GM_9BXX_EPS_TMS570/SwProject/TMS570LS202x6SFlashLnk.cmd` defines the Flash and RAM section layout for the TMS570LS20216 device (big-endian). It must stay consistent with the Non-Volatile Memory block layout, the calibration placement, and the Error Correcting Code coverage.

## Post-build script

`GM_9BXX_EPS_TMS570/SwProject/postbuild.bat` (Windows host) takes the linked `.out` file base name and:

1. Deletes stale `.hex` artifacts.
2. Runs the Checksum Correction Tool over the `.out` image.
3. Generates Intel-hex and map files with `hex470`.
4. Runs `apmem.vbs` (memory-footprint accounting) against the ECU configuration.

See the [Build System](../general/build-system/) page for the full build procedure.
