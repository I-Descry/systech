# Insufficient Storage Issue - Disk Space Cleanup Using TreeSize

## Overview

A user was unable to download important company files and experienced system lag due to insufficient disk space. Basic cleanup methods were initially performed but only provided minimal storage recovery, requiring deeper analysis using **TreeSize** to identify large hidden files consuming storage.

---

## Issue Description

The user reported that the desktop was running slowly and could not download important company files because the system drive had very limited free space.

Initial cleanup methods were performed, such as accessing temporary folders via **Run** (`Win + R`), such as `%temp%`, `temp`, and `prefetch`, along with emptying the Recycle Bin, running Disk Cleanup, and uninstalling unused applications. However this actions only recovered a fraction amount of storage.

Further troubleshooting and investigation was required to locate hidden large files occupying disk space.

---

## Scope / Impact

- **Affected:** Single User
- **System/Device:** Windows Desktop (`C:Drive/Local Storage`)
- **Service:** Unable to download files and perform normal file operations
- **Performance:** System slowdown due to low disk space
- **Productivity:** Reduced user efficiency due to storage limitations

---

## Analysis / Troubleshooting Steps

- Verified user report: inability to download files and system lag
- Checked system drive (`C:`) storage status
  - Confirmed critically low available disk space
- Identified that performance degradation is consistent with low storage condition
- Performed initial storage cleanup:
  - Accessed temporary file locations via **Run** (`Win + R`):
    - `%temp%` → deleted user temporary files
    - `temp` → cleared Windows temporary files
    - `prefetch` → cleared system prefetch cache
  - Emptied Recycle Bin to free deleted file storage
  - Executed Windows Disk Cleanup Utility
  - Uninstalled unused applications via **Control Panel** → Programs and Features
- Rechecked disk space after cleanup
  - Observed only minimal improvement in available storage
- Determined that standard cleanup methods were insufficient
- Hypothesized presence of hidden large files or non-obvious storage consumption
- Installed and executed **TreeSize** for detailed disk usage analysis
- Performed full scan of system drive (`C:`)
- Identified abnormal storage consumption in:
  - Large user directories
  - Application data folders
  - Hidden files
  - System-generated files
- Validated that identified directories were primary contributors to disk usage

---

## Resolution

- Used **TreeSize** to perform detailed storage analysis
- Identified unnecessary large files and directories
- Removed safe-to-delete files and unnecessary data
- Cleaned residual files from user folders and application data
- Verified that available disk space increased significantly
- Retested system performance and file download functionality

---

## Outcome

- Sufficient disk space was restored
- User was able to download important company files successfully
- System performance improved and lag was reduced
- Desktop returned to normal operational state

---

## Root Cause

Hidden large files and accumulated unnecessary data were consuming significant disk space, resulting in insufficient storage and degraded system performance.

Basic cleanup methods were not sufficient as the majority of storage usage came from deeper user directories and hidden application data.

---

## Recommendations

- Perform regular disk space monitoring on user workstations
- Use tools like **TreeSize** for deeper storage analysis when standard cleanup is insufficient
- Educate users on proper file and download management
- Regularly review Downloads, Desktop, and AppData folders for large files
- Maintain sufficient free disk space for system stability

---

## Notes

- Issue was storage-related, not hardware failure
- Standard cleanup methods may not detect all large hidden files