**## Overview**



A desktop were unable to print to a shared network printer because the host PC (printer server) was configured with **Metered Network Connection**.



\-------



**## Issue Description**



* Users cannot send print jobs to the shared printer
* Printer appears online but there is no print job process
* Other devices are connected to the network but printing fails



\-------



**## Analysis**



* Checked printer status on host PC → Online
* Verified both host PC and Users network connectivity → Same network connectivity
* Tested `ping` between devices → Successful
* Checked print spooler service → Running
* Identified host PC network settings → **Metered Connection Enabled**



\-------



**## Root Cause (Suspected)**



This is the first recorded occurrence of the issue on the host PC. The cause may be related to a system-level or network configuration change.



**# Impact**



* Print job process
* Communication between host PC (printer server) and User



\-------



**## Resolution**



* Disabled **Metered Connection** on host PC (printer server):

  1. Settings → Network \& Internet → Wi-Fi/Ethernet
  2. Turn off "Set as **metered connection**"
* Tested printing from User after applying the change



\-------



**## Outcome**



* Printer became accessible to all Users
* Print jobs processed normally
* Network printing functionality restored



\-------



**## Notes / Prevention**



* Ensure host PC (server printer) used as print servers are not set to Metered Connection
* Avoid restricting network services on shared resources



\-------



**## Related Topics**



* Printer sharing over network
* Print Spooler service troubleshooting
* Windows network settings









