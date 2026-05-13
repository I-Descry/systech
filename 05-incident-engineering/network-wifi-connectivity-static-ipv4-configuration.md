# Incident Report - Wi-Fi Connectivity Failure Due to Static IPv4 Configuration

## Overview

A user laptop was unable to access the internet through Wi-Fi connectivity, while wired Ethernet connection was functioning normally.

---

## Issue Description

The laptop could connect to the Wi-Fi network but was unable to access the internet. However, internet connectivity was working properly when connected through Ethernet.

This indicated that the issue was isolated to the wireless network configuration of the device.

---

## Scope / Impact

- **Affected:** Single User Laptop
- **Setup:** Wireless Network (Wi-Fi) and Ethernet connectivity
- **Impact:** User unable to access internet through Wi-Fi connection

---

## Analysis / Troubleshooting Steps

- Verified internet connectivity through Ethernet connection
- Confirmed issue only occurs when using Wi-Fi
- Checked wireless adapter status
- Reviewed IPv4 network configuration settings
- Identified that IPv4 configuration was manually assigned (static)
- Determined manual IPv4 configuration was incompatible with current network environment

---

## Resolution

### Step-by-Step Resolution Process

### 1. Open Network Connections

Navigate to:

- Control Panel > Network and Internet > Network and Sharing Center > Change Adapter Settings

---

### 2. Open Wi-Fi Adapter Properties

- Right-click the Wi-Fi adapter > Select **Properties**

---

### 3. Open IPv4 Configuration

- Select:

`Internet Protocol Version 4 (TCP/IPv4)`

- Click **Properties**

---

### 4. Identify Incorrect Manual Configuration

Observed that the Wi-Fi adapter was configured with manually assigned IPv4 settings instead of automatic DHCP configuration.

Examples of manually configured values may include:

- Static IP Address
- Subnet Mask
- Default Gateway
- Preferred DNS Server
- Alternate DNS Server

---

### 5. Revert Configuration to Automatic

Select:

- **Obtain an IP address automatically**
- **Obtain DNS server address automatically**

Then:

- Click **OK**
- Close all network windows

---

### 6. Reconnect to Wi-Fi

- Disconnect from Wi-Fi
- Reconnect to the wireless network
- Verify internet connectivity

---

## Outcome

- Laptop successfully connected to the internet through Wi-Fi
- Network connectivity restored without requiring Ethernet connection
- User regained normal wireless internet access

---

## Root Cause

Incorrect manually configured IPv4 settings preventing proper DHCP network configuration and internet connectivity over Wi-Fi.

---

## Recommendations

- Use automatic IPv4 configuration (DHCP) unless static addressing is specifically required
- Verify network adapter settings during connectivity troubleshooting
- Document static IP configurations before modifying them
- Avoid unnecessary manual network configuration changes on user devices

---

## Notes

- Ethernet connectivity helped isolate the issue to wireless network configuration
- Issue was configured-related, not hardware-related
- Restoring DHCP settings resolved the connectivity issue immediately

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.2 | 05/13/2026 | Refined technical wording |
| 1.1 | 05/13/2026 | Added detailed step-by-step resolution process and IPv4 configuration clarification |
| 1.0 | 05/13/2026 | Initial version |