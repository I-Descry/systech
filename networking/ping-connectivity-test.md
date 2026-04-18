**## Overview**



The `ping` command is use to test network connectivity between the device and a target IP Address or hostname. It verifies whether a device is reachable over the networking using ICMP requests.



\-------



**## How to Use**



1. Open Command Prompt (CMD)
2. Type:
`ping` *IP address*
3. Enter



\-------



**## Example**



`ping` *IP Address*

`ping` 192.168.1.1



\-------



**## Purpose**



* Check if a device is online or reachable
* Test basic network connection
* Identify packet loss issues
* Measure latency (response time)



\-------



**## Results**



**# Successful Reply / Host Reachable**



Reply from 192.168.1.1: bytes=32 time<1ms TTL=64



**# Meaning**



* Device is reachable
* Network connection is working



\---



**# Request Timed Out / No Response**



Request timed out.



**# Meaning**



* Device is unreachable
* Possible Causes:

  1. Wrong IP Address
  2. Device is offline
  3. Device is powered off
  4. Network cable disconnected
  5. Firewall blocking ICMP



\---



**# High Latency / Slow Response**



time=150ms



**# Meaning**



* Slow or unstable network
* Possible congestion
* Wi-Fi issue



\-------



**# Common Use Cases**



* Checking printer connectivity (host and user connection)
* Verifying server accessibility
* Testing LAN connection
* Basic network troubleshooting



\-------



**# Notes / Limitations of `ping`**



* `ping` command only tests basic network connectivity (Layer 3 - ICMP)
* Some devices block `ping` (ICMP request) for security reasons
* A successful `ping` does NOT guarantee services are 100% working (printer, web server, database, etc.)
* `ping` does not test application-level issues



\-------



**# Related Commands**



* `ipconfig` → check IP address and gateway
* `tracert` → trace network path
* `nslookup` → test DNS resolution





