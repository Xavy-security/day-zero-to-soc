# Lab 01 - Network Connectivity Check
**Date:** 2026-10-06 | **Location:** Salitrillos, CR | **Analyst:** Xavy
**Tools:** Windows CMD - ping, nslookup

## Objective
Verify connectivity and DNS resolution - first step of any SOC investigation.

## Commands Executed
ping 8.8.8.8
nslookup google.com
## Results
- **Ping 8.8.8.8:** 4 packets sent, 4 received, 0% loss
    - Min 55ms, Max 65ms, Avg 60ms, TTL 113
    - Interpretation: Stable connection to Google DNS
- **NSLookup google.com:** 
    - IPv4: 142.251.215.14
    - IPv6: 2607:f8b0:4008:808::200e

## Security Insight
- Baseline 0% loss is normal. If I see >10% loss in future = possible DDoS or network issue.
- TTL 113 helps identify OS and distance of target.
- DNS resolution is first step in threat hunting.

## English Summary
Today I verified connectivity to Google DNS (8.8.8.8). Zero packet loss indicates a stable connection. I also resolved google.com to its IP address 142.251.215.14. This is fundamental for SOC analysis.
