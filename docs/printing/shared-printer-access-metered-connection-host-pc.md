# Shared Printer Access Issue - Metered Connection on Host PC

## Overview

A desktop were unable to print to a shared network printer because the host PC (printer server) was configured with **Metered Network Connection**.

---

## Issue Description

Users were unable to print to the host PC (printer server). Although the printer appeared online, no print jobs were processed.

---

## Scope / Impact

- **Affected:** Multiple Users
- **Setup:** Shared printer via host PC (printer server)
- **Impact:** Users unable to print over the network

---

## Analysis / Troubleshooting Steps

- Checked printer status on host PC (printer server) → Online
- Verified network connectivity between host and users → Same network
- Tested `ping` between devices → Successful
- Checked **Print Spooler service via `service.msc`** → Running
- Identified host PC (printer server) network configuration → **Metered Connection Enabled**

---

## Resolution

- Disabled **Metered Connection** on the host PC (printer server):
  - Settings → Network & Internet → Wi-Fi/Ethernet
  - Turn off **Set as metered connection**
- Verified network communication between devices
- Retested printing from user devices

---

## Outcome

- Printer became accessible to all users
- Print jobs processed successfully
- Network printing functionality restored

---

## Root Cause

Metered network configuration on the host PC (printer server) restricting network services, preventing proper sharing and communication.

---

## Recommendations

- Avoid enabling **Metered Connection** on systems acting as print servers
- Ensure shared resources are on unrestricted network profiles
- Standardize network configurations for shared devices

---

## Notes

- Issue was **network configuration-related**, not printer or driver issue
- Metered connection can limit background services, including printer sharing