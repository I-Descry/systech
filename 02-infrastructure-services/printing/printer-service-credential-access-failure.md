# Shared Printer Access Issue - Credential Authentication Required

## Overview

A desktop (remote branch) was unable to access a shared network printer host PC (printer server) due to credential authentication requirements.

---

## Issue Description

The shared printer was not visible or accessible from the desktop (remote branch), preventing users from printing documents.

---

## Scope / Impact

- **Affected:** Remote branch user
- **Setup:** Printer shared via server PC
- **Impact:** Unable to access and use shared printer

---

## Analysis / Troubleshooting Steps

- Verified printer is physically connected to the host PC (printer server)
- Checked printer sharing was enabled
- Identified server `hostname`
- Attempted access to shared → **Required Credentials**
- Determined authentication was required for access

---

## Resolution

- Retrieved correct **username and password** from the host PC (printer server)
- Opened **Credential Manager** on the desktop (remote branch):
  - Press `Windows + R` → type `control` → press Enter
  - Navigate to **User Accounts** → **Credential Manager**
  - Select **Windows Credentials**

- Added sample network credentials:
  - Click **Add a Windows credential**
  - Enter the following:
    - Internet or Network address: `\\DESKTOP-EXAMPLE` or `\\IP Address`
    - User name: `<username>`
    - Password: `<password>`

- Access shared resources:
  - Press `Windows + R`
  - Enter: `\\DESKTOP-EXAMPLE` or `\\IP Address`

- Connected to the shared printer

---

## Outcome

- Remote desktop successfully connected to the host PC (network printer)
- Printer became accessible and usable
- Printing functionality restored to the desktop user (remote branch)

---

## Root Cause

Missing or incorrect network credentials preventing access to the shared printer on the server PC.

---

## Recommendations

- Ensure proper credential sharing for network resources
- Pre-configure credentials for remote users if required
- Use consistent user accounts across network environments
- Document server hostnames and access credentials securely

---

## Notes

- Issue was **authentication-related**, not network or hardware
- Credential Manager is essential for accessing secured shared resources

