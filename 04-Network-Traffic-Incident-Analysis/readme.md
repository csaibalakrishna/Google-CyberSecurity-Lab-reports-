# Network Traffic Incident Analysis

## Overview

This lab focuses on investigating a network connectivity issue by analyzing packet capture data using `tcpdump`.

The objective was to examine captured network traffic, identify the source of communication failures, determine the affected network protocol, and provide a technical assessment of the incident.

---

## Objective

- Analyze captured network traffic.
- Interpret TCP/IP protocol behavior.
- Investigate DNS communication failures.
- Identify possible causes of the incident.
- Recommend appropriate next steps for investigation.

---

## Scenario

Users reported that they were unable to access a website and received a **"Destination Port Unreachable"** error.

A packet capture was collected using **tcpdump** to investigate the issue and determine whether the problem originated from the client, network infrastructure, or DNS server.

---

## Tools Used

- tcpdump
- DNS
- UDP
- ICMP

---

## Security Concepts

- Network Traffic Analysis
- DNS Resolution
- UDP Communication
- ICMP Error Messages
- Packet Capture Analysis
- Incident Investigation
- Network Troubleshooting

---

## Investigation Summary

Analysis of the packet capture identified repeated DNS requests sent over UDP to port 53.

Instead of receiving valid DNS responses, the client received ICMP error messages indicating that **UDP port 53 was unreachable**.

These findings suggest that DNS communication failed before successful name resolution could occur.

---

## Technical Findings

The investigation identified the following observations:

- DNS requests were transmitted using UDP.
- ICMP responses indicated **Destination Port Unreachable**.
- DNS server communication was unsuccessful.
- Website name resolution could not be completed.
- The network issue affected user access to the requested service.

---

## Root Cause Analysis

Based on the available evidence, several possible causes were identified:

- DNS server outage
- Firewall blocking UDP port 53
- DNS service misconfiguration
- Denial-of-Service (DoS) attack affecting the DNS server

Further investigation would be required to determine the exact root cause.

---

## Recommended Next Steps

- Verify DNS server availability.
- Confirm that UDP port 53 is reachable.
- Review firewall rules affecting DNS traffic.
- Inspect DNS server logs.
- Monitor for abnormal network activity that may indicate a denial-of-service attack.

---

## Skills Demonstrated

- Network Traffic Analysis
- Packet Capture Analysis
- tcpdump
- DNS Troubleshooting
- ICMP Analysis
- Incident Investigation
- Root Cause Analysis
- Technical Documentation

---

## Key Takeaways

This exercise demonstrated how packet capture analysis can be used to diagnose network communication failures.

Understanding protocol interactions between DNS, UDP, and ICMP enables security analysts to identify connectivity problems, distinguish between network and application-layer issues, and guide further incident response activities.

---

## Supporting Document

The original incident analysis report completed during the Google Cybersecurity Professional Certificate is included in this directory for reference.
