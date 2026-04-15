**## Overview**



A desktop (remote branch) was unable to print documents from a browser-based application accessed via SSO.



\-------



**## Issue Description**



The browser print dialog appeared normally, but no print job was processed after confirming the print action, preventing the user from printing documents.



\-------



**## Analysis**



* Checked Print Spooler service via `services.msc`
* Verified printer connectivity on the desktop (remote branch)
* Confirmed issue was isolated to browser-related printing (Google Chrome), not the printer or system itself
* Identified possible browser-related issue (cache or extension interference)



\-------



**## Resolution**



* Restarted Print Spooler service
* Cleared browser cache and stored data
* Disabled and removed background browser extensions
* Retested printing functionality within the browser



\-------



**## Outcome**



* Browser-based printing successfully restored
* Print jobs were processed correctly from the SSO system
* User regained full printing functionality on the desktop (remote branch)



