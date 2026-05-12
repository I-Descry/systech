# Incident Report - HP Canon MF Network Printer Offline Issue (Scanner Selector Disabled)

---

## Overview

Network printer appears offline due to Canon MF Network Scanner Selector being disabled, causing loss of printer connectivity even when network and credentials are correct.

---

## Issue Description

Users reported that the **HP Network Printer** shows as **Offline**, preventing printing and scanning functions.

Upon checking, the Canon MF Network Scanner Selector was found to be **Unchecked**, which results in the printer not being properly recognized over the network.

---

## Scope / Impact

- **Affected:** Single User
- **Setup:** HP Canon MF Network Printer (Network/Shared via host PC)
- **Impact:**
  - Printer appears offline on the User (Excel, Word, etc.) when printing
  - Printing and scanning functions unavailable
  - User workflow interruption

---

## Analysis / Troubleshooting Steps

- Checked Canon MF Network Scanner Selector on affected system
- Found that the scanner selector was **Unchecked**
- Checked the correct Printer Name and MAC Address on the Scanner List of Canon MF Network Scanner Selector
- Rechecked printer status and connectivity

---

## Resolution

- Enabled Canon MF Network Scanner Selector
- Restored network registration of the printer
- Printer connection successfully reconnected

---

## Outcome

- HP printer returned to online status
- User regained printing and scanning access
- Issue resolved after enabling scanner selector

---

## Root Cause

- The Printer Name and MAC Address of the host PC printer in Canon MF Network Scanner Selector was Unchecked

Cause is currently unclear:

- Possible accidental user action
- Possible software or system reset behavior

---

## Recommendations

- Ensure Canon MF Network Scanner Selector remains enabled after setup
- Avoid disabling network scanner components
- Monitor after updates or system changes
- Standardize printer configuration for Canon MF devices

---

## Notes

- Issue is intermittent
- Further monitoring needed to determine exact trigger

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.0 | 2026-05-12 | Initial incident report created |