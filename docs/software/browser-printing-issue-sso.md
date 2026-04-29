# SSO Browser Printing Issue - SSO Application (Chrome/Microsoft Edge)

## Overview

A desktop (remote branch) was unable to print documents from a browser-based application accessed via Single Sign-On (SSO).

---

## Issue Description

The browser print dialog appeared normally, but no print job was processed after confirming the print action, preventing user from printing documents.

---

## Scope / Impact

- **Affected:** Single user (remote branch)
- **System:** Browser-based Single Sign-On (SSO) application
- **Browser:** Google Chrome & Microsoft Edge
- **Impact:** User unable to print documents

---

## Analysis / Troubleshooting Steps

- Checked **Print Spooler service** via `services.msc`
- Verified printer status:
  - Installed correctly  
  - Set as default  
  - Online and reachable
- Tested printing outside the Google Chrome and Microsoft Edge browser (Test Page) → Working
- Tested printing across multiple browsers → Not Working
- Confirmed the issue was isolated to browser-based printing only (Google Chrome & Microsoft Edge)
- Identified a potential browser-related issue (cache or extension interference)
- Reviewed browser environment:
  - Cache and stored data
  - Installed extensions

---

## Resolution

- Disabled or removed unnecessary **browser extensions**
- Restarted the browser
- Retested printing functionality within the browser

---

## Outcome

- Browser-based printing was successfully restored
- Print jobs were processed correctly from the SSO application
- User regained full printing functionality on the desktop

---

## Root Cause

Browser cache corruption or conflicting extensions interfering with print processing.

---

## Recommendation

- Avoid installing unnecessary browser extensions
- Regularly review and manage installed browser extensions
- Regularly clear browser cache for shared or frequently used systems
- Limit unnecessary browser extensions in production environments
- Keep browsers updated to avoid compatibility issues

---

## Notes

- Issue is **browser-related**, not printer hardware or network
- Successful test page confirms printer and driver are working properly