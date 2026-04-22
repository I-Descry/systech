# Ping Command - Network Connectivity Test

## Overview

The `ping` command is used to test network connectivity between a device and a target IP address or hostname. It verifies whether a device is reachable over the network using ICMP requests.

---

## How to Use

1. Open Command Prompt (CMD)
2. Type: `ping <IP Address>`
3. Press Enter

---

## Example

`ping` *IP Address*
`ping` 192.168.1.1

---

## Purpose

- Check if a device is online or reachable  
- Test basic network connectivity  
- Identify packet loss issues  
- Measure latency (response time)  

---

## Results

### Successful Reply / Host Reachable

Reply from 192.168.1.1: bytes=32 time<1ms TTL=64

**Meaning:**
- Device is reachable  
- Network connection is working  

---

### Request Timed Out / No Response

Request timed out.

**Meaning:**
- Device is unreachable  

**Possible Causes:**
- Wrong IP address  
- Device is offline  
- Device is powered off  
- Network cable disconnected  
- Firewall blocking ICMP  

---

### High Latency / Slow Response

Reply from 192.168.1.1: bytes=32 time=150ms TTL=64

**Meaning:**
- Slow or unstable network  
- Possible congestion  
- Wi-Fi issues  

---

## Common Use Cases

- Checking printer connectivity (host and client)  
- Verifying server accessibility  
- Testing LAN connection  
- Performing basic network troubleshooting  

---

## Notes / Limitations of `ping`

- `ping` only tests basic network connectivity (Layer 3 - ICMP)  
- Some devices block ICMP requests for security reasons  
- A successful `ping` does **not** guarantee that services are working (printer, web browser, database, etc.)

---

## Related Commands

- `ipconfig` → Check IP address and default gateway  
- `tracert` → Trace the path packets take to a destination  
- `nslookup` → Test DNS resolution  

---

## Notes

This document is intended for basic network troubleshooting and IT support reference :D