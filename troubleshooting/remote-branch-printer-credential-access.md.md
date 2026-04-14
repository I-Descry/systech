**## Overview**



A desktop (remote branch) was unable to access a shared network printer hosted on a server PC.



\-------



**## Issue Description**



The printer was not visible or accessible from the desktop (remote), preventing Users from printing documents.



\-------



**## Analysis**



* Checked the server PC where the printer is physically connected
* Verified printer sharing was enabled
* Identified the server hostname
* Confirmed valid User credentials were required to access



\-------



**## Resolution**



* Accessed server PC to retrieve correct Username and Password
* Configured Windows Credential Manager on the remote device
* Added Network Credential using (hostname): `\\DESKTOP-EXAMPLE`
* Opened run dialog (`Windows Key + R`)
* Entered (hostname) `\\DESKTOP-EXAMPLE` to access shared resources
* Connected it to the shared network printer



\-------



**## Outcome**



* Remote device successfully connected to the network printer
* Printing functionality restured to the desktop user (remote branch)

