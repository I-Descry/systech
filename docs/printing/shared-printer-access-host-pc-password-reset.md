# Shared Printer Access Issue - Host PC Password Reset

## Overview

A desktop (remote branch) were unable to print to a shared network printer because the host PC (printer server) credentials were no longer valid. The issue occurred when the local administrator account password on the host PC (printer server) was changed or reset, preventing authentication from remote users.

---

## Issue Description

Users were unable to connect to the host PC (shared printer). When attempting to access the shared resource using the hostname or IP address, authentication failed due to incorrect or outdated credentials. This prevent users from printing documents.

---

## Scope / Impact

- **Affected:** Multiple Users (remote branch users)
- **Setup:** Shared printer connected to host PC (printer server)
- **Access Method:** Network printer via hostname and shared credentials
- **Impact:** Users unable to connect to and use the shared printer

---

## Analysis / Troubleshooting Steps

- Verified printer was physically connected to the host PC (printer server)
- Confirmed printer sharing was enabled on the host PC (server printer)
- Tested network connectivity between remote user and host PC → Working
- Verified hostname access using:
  - `\\hostname` or `\\IP Address` → Credential prompt appeared
- Identified authentication failure due to invalid saved credentials
- Changed remote control from user to host PC (printer server)
- Checked the host PC local administrator account credentials
- Confirmed the administrator password has been changed or reset

---

## Resolution

- Remoted into the host PC (printer server)
- Opened **Command Prompt (CMD)** with administrator privileges
- Reset the local user account password using:

```cmd
net user USER newpassword
```

- Updated saved credentials on the remote user's desktop using **Credential Manager**
- Reconnected to the shared resource using:
  - `\\hostname` or `\\IP Address`
- Retested shared printer access and printing functionality

---

## Outcome

- Remote users successfully reconnected to the shared printer
- Authentication was restored
- Printing functionality resumed normally

---

## Root Cause

Credential mismatch caused by the local administrator account password on the host PC being changed, reset, or expired.

Possible causes may include:

- Windows password expiration policy
- Domain Group Policy enforcement
- Manual password changes by users or other IT staff
- Credential mismatch from outdated saved passwords

---

## Recommendations

- Use a dedicated printer-sharing account instead of the default administrator account
- Disable password expiration of the host PC (printer server)
- Maintain secure documentation of printer server credentials
- Standardize shared printer credentials across remote branches
- Regularly verify remote printer access to prevent repeated incidents

---

## Notes

- Issue was **authentication-related**, not printer hardware or network connectivity
- Credential Manager should be updated whenever shared account passwords are changed
- Using a dedicated account password for host PC (printer server) is recommended for long-term stability