---
title: "Customer Diagnostic Services"
description: "Vehicle-specific diagnostic services."
---
# Customer Diagnostic Services


## Purpose and responsibility

`GM_9BXX_EPS_TMS570/SwProject/CMS_9Bxx/` carries the vehicle-line-specific diagnostic services: the customer side of the International Organization for Standardization services, the Measurement and Calibration Protocol interface, and the service look-up table implementation. It builds on the shared [Common Diagnostic Services](../bsw/cms_common/) implementation.

## Layout

| Location | Content |
| --- | --- |
| `CMS_9Bxx/include/` | Customer/Interface headers for ISO and XCP services |
| `CMS_9Bxx/src/` | Customer service implementation and the service look-up table |
