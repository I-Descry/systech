# Shared Printer Access Issue - Printer Sharing Disabled

## Overview

A desktop (remote branch) were unable to print documents because the shared printer on the host PC (printer server) was no longer accessible. The issue occurred when the printer sharing option in the printer properties was unexpectedly disabled.

---

## Issue Description

Users were unable to send print jobs to the shared network printer. Although the printer driver was installed and connected to the host PC (printer server), the shared printer was not visible or accessible from remote desktops. This prevented users from printing documents through the network printer.

---

## Scope / Impact

- **Affected:** Multiple Users (remote branch users)
- **Setup:** Shared printer connected to host PC (printer server)
- **Access Method:** Network shared printer
- **Impact:** Users unable to print through the shared printer

---

## Analysis / Troubleshooting Steps

- Verified printer was powered on and functioning locally on the host PC (printer server)
- Confirmed network connectivity between remote users and the host PC (printer server) → Working
- Tested printer access using 
  - `\\hostname`` or `\\IP Address` → Printer not accessible
- Checked **Device and Printers** on the host PC (printer server)
- Opened **Printer Properties** → **Sharing** tab
- Identified that the option **Shared this printer** was unchecked
- Confirmed printer sharing had been disabled, preventing remote access

---

## Resolution

- Accessed the host PC (printer server)
- Opened **Control Panel** → **Devices and Printers**
- Right-clicked the printer → **Printer Properties**
- Opened the **Sharing** tab
- Enabled/Checked **Sharing this printer**
- Verified the correct share name was configured
- Retested printing from remote users

---

## Outcome

- Shared printer became visible to remote users
- Print jobs were successfully processed
- Network printing functionality was restored

---

## Root Cause

Printer sharing was disabled in the printer properties, preventing remote devices from accessing the shared printer.

Possible causes may include:

- Windows updates modifying printer settings
- Printer driver reinstallation resetting sharing configuration
- Manual changes by Users or IT staff
- System configuration reset after restart or maintenance

---

## Recommendations

- Regularly verify printer sharing settings on host PCs used as print servers
- Restrict unauthorized changes to printer properties
- Maintain standard printer sharing configurations
- Recheck sharing settings after driver updates or system maintenance

---

## Notes

- Issue was **sharing configuration-related**, not network or hardware related
- Local printing on the host PC (printer server) remained functional even when sharing was disabled
- Shared printer settings should be included in routine printer maintenance checks
- Issue was **authentication-related**, not printer hardware or network connectivity
- Credential Manager should be updated whenever shared account passwords are changed
- Using a dedicated account password for host PC (printer server) is recommended for long-term stability