---
title: "Build System"
description: "Code Composer Studio project, linker, and post-build tooling."
---
# Build System

There are no Makefiles or CMake files in the repository. The build is a **Texas Instruments Code Composer Studio** (Eclipse/CDT managed-build) project that invokes the CCS toolchain's `gmake`.

## Build inputs

| Artifact | Path (repository-relative) | Role |
| --- | --- | --- |
| Eclipse/CDT project | `GM_9BXX_EPS_TMS570/SwProject/.project`, `.cproject`, `.ccsproject` | Project definition: device `TMS570LS20216`, big-endian (`be32`), Code Generation Tools 4.6.4, ELF output, `gmake -j4 -s -k` managed build. |
| Linker command file | `GM_9BXX_EPS_TMS570/SwProject/TMS570LS202x6SFlashLnk.cmd` | Flash/RAM section layout for the 20216 device. |
| Post-build script | `GM_9BXX_EPS_TMS570/SwProject/postbuild.bat` | Converts the `.out` image: runs the Checksum Correction Tool, generates Intel-hex via `hex470`, and runs the memory-footprint script (`apmem.vbs`) against the ECU configuration. |
| Generated configuration | `GM_9BXX_EPS_TMS570/SwProject/Source/GenData*`, `Header/` | DaVinci/RTE cannot be rebuilt from this repository alone; the checked-in generated files are the build inputs. A full regeneration additionally requires the Vector DaVinci Configurator toolchain, which is not part of this repository. |

## How to build

1. Install Texas Instruments Code Composer Studio with the Hercules TMS570 code generation tools (the project targets Code Generation Tools 4.6.4).
2. Import `GM_9BXX_EPS_TMS570/SwProject` as an existing CCS project.
3. Build the `all` target from the IDE (managed `gmake`).
4. Run `postbuild.bat` with the output file base name to produce the flashable hex artifacts.

:::caution[Host tooling]
The post-build step depends on Windows host tools (`CCT`, `hex470`, `hexview`, `cscript`/`apmem.vbs`) referenced by relative paths. Building on Linux documents the software but does not reproduce the production flash image.
:::

## Continuous integration

No workflow files exist in the repository, so there is no automated build to describe. The documentation site (this site, sourced from `docs/`) is the only build verified here; see the repository readme for how to build it.
