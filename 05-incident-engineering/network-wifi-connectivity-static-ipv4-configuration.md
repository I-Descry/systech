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

- Opened network adapter IPv4 settings
- Removed manually configured IPv4 values
- Reverted IPv4 configuration back to automatic assignment (DHCP)
- Reconnected laptop to Wi-Fi network
- Verified successful internet connectivity

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
| 1.0 | [Date] | Initial version |