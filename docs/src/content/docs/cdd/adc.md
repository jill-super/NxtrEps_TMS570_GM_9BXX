---
title: "Analog-to-Digital Converter Driver (Adc)"
description: "Complex Device Driver for Analog-to-Digital Converter Unit 1: result-memory layout, buffer allocation checks, and threshold interrupts (TMS570 ADC)."
---

# Analog-to-Digital Converter Driver

Directory: `Adc` · AUTOSAR group: Complex Device Drivers


## Purpose and responsibility

Complex Device Driver for Analog-to-Digital Converter Unit 1: result-memory layout, buffer allocation checks, and threshold interrupts (TMS570 ADC).

## Source layout

Repository path: `Adc/`

| File | Role |
| --- | --- |
| `Adc/src/Adc.c` | Implementation |
| `Adc/src/Adc2.c` | Implementation |
| `Adc/src/Adc_Common.c` | Implementation |
| `Adc/include/Adc.h` | Public header |
| `Adc/include/Adc2.h` | Public header |
| `Adc/include/Adc_Common.h` | Public header |


## Public interface

No top-level symbols were extracted automatically; the public interface is defined by the module header and the Run-Time Environment contract. See the source files listed above.


## Dependencies

- `Adc.h`
- `Adc2.h`
- `Adc_Common.h`
- `Ap_DiagMgr.h`
- `CDD_Data.h`
- `CalConstants.h`
- `Calconstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `SystemTime.h`


## Configuration and usage

Initialized during Electronic Control Unit startup and scheduled by the Run-Time Environment/Basic Scheduler. Register-level details are in the driver sources and the TMS570 reference documentation.
