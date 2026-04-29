# TreeSize - Disk Usage Analysis Tool

## Overview

TreeSize is a versatile disk space analysis utility used to scan storage volumes and provide a hierarchical breakdown of file and folder usage. It reads file system data from NTFS (or other supported file systems) and calculates the disk usage based on the total size of directories. The tool is commonly used for diagnosing low disk space issues, identifying large or hidden files, and supporting system cleanup operations in Windows environments.

TreeSize is available in Free and Pro editions, where the Free version provides basic disk usage analysis, while the Pro version includes advanced features such as detailed reporting, automation, and extended file system support.

---

## Purpose

- Perform detailed disk usage analysis on local or network drives
- Identify large files, folders, and hidden storage consumption
- Support troubleshooting of low disk space issues
- Assist in system cleanup and storage optimization
- Provide visibility into storage distribution across directories

---

## When to Use TreeSize

TreeSize is typically used in the following scenarios:

- System drive (`C:`) is critically low on storage
- User cannot download, install, or save files
- System performance is degraded due to low disk space
- Standard cleanup methods are insufficient:
  - Temporary files cleanup
  - Disk cleanup utility
  - Uninstalling applications
- Need to identify hidden or non-obvious large files
- Storage audit or workstation maintenance is required

---

## Key Features

- Hierarchical disk usage visualization (tree structure)
- Folder size calculation based on contained files
- Sorting by size to identify top storage consumers
- Detection of hidden and system directories
- Scanning of local and network drives
- Exportable scan results (depending on version)

---

## How It Works (Technical Behavior)

- Scans file system starting from selected root directory (e.g., `C:\`)
- Reads file metadata from NTFS file system
- Calculates folder sizes recursively
- Aggregates file sizes into parent directories
- Displays results in hierarchical tree format
- Does not modify or alter file system data

---

## IT Use Cases

- Troubleshooting insufficient disk space issues
- Investigating system slowdown due to storage pressure
- Identifying large user-generated files (downloads, videos, backups)
- Detecting application cache and residual data
- Performing storage audits on endpoints or workstations
- Supporting system cleanup operations in IT environments

---

## Limitations

- Does not delete or modify files (read-only tool)
- Requires appropriate permissions for system directories
- May not fully scan restricted or protected folders without admin access
- Some system or locked files may not display accurate size without elevation

---

## Notes

- TreeSize operates as a read-only disk analysis tool and does not perform any system changes.
- Administrator privileges may be required to access system-protected directories such as:
  - `C:\Windows`
  - `Program Files`
  - `AppData`
- Results should always be reviewed carefully before taking deletion actions.
- Some large files identified may be required by the system or installed applications.
- Best used after standard cleanup methods (Disk Cleanup, Temp folder cleanup, uninstalling applications).