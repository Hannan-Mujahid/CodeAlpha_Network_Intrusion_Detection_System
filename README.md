# CodeAlpha Task 4: Network Intrusion Detection System (NIDS)

## Overview
This repository contains the configuration and custom rule set for Snort IDS to monitor network traffic and trigger real-time alerts for ICMP Echo Requests (pings).

## Technologies Used
- **OS:** Kali Linux
- **IDS Tool:** Snort 3
- **Network Interface:** wlan0

## Custom Snort Rules
Custom rules added to `/etc/snort/rules/local.rules`:

```snort
alert icmp any any -> any any (msg:"[ALERT] IPv4 Ping Detected"; itype:8; sid:1000001; rev:2;)
alert icmp any any -> any any (msg:"[ALERT] IPv6 Ping Detected"; itype:128; sid:1000002; rev:1;)
