# SYN Flood Attack Analysis

## Overview

This lab investigates a network service disruption caused by a Denial-of-Service (DoS) attack. The objective was to analyze network behavior, identify the attack type, and explain how the attack affected the availability of the web server.

---

## Objective

- Identify the type of network attack.
- Analyze the behavior of TCP connections.
- Explain how the attack impacts server availability.
- Understand the TCP three-way handshake.
- Recommend mitigation strategies.

---

## Scenario

A website became inaccessible and users experienced **connection timeout** errors.

Network logs showed a large number of incomplete TCP connection requests, requiring an investigation to determine the cause of the service disruption.

---

## Security Concepts

- Denial-of-Service (DoS)
- SYN Flood Attack
- TCP Three-Way Handshake
- Network Availability
- TCP Connections
- Network Attack Analysis
- Incident Investigation

---

## Attack Analysis

The investigation determined that the interruption was consistent with a **SYN Flood attack**.

The attacker continuously transmitted large numbers of TCP SYN packets without completing the TCP connection process.

As a result, the web server allocated resources for half-open connections until its connection table became exhausted.

Once server resources were depleted, legitimate users could no longer establish new connections.

---

## TCP Three-Way Handshake

A normal TCP connection follows three steps:

1. Client sends a **SYN** packet requesting a connection.
2. Server responds with a **SYN-ACK** packet.
3. Client replies with an **ACK** packet, completing the connection.

During a SYN Flood attack, the attacker intentionally omits the final ACK, leaving numerous half-open connections that consume server resources.

---

## Impact

The attack resulted in:

- Connection timeout errors
- Resource exhaustion
- Denial of service for legitimate users
- Reduced website availability

---

## Possible Mitigation Strategies

- Enable SYN Cookies.
- Configure firewall rate limiting.
- Deploy Intrusion Prevention Systems (IPS).
- Implement DDoS protection services.
- Monitor abnormal TCP connection patterns.
- Increase server resilience against connection flooding.

---

## Skills Demonstrated

- Network Attack Analysis
- TCP/IP Fundamentals
- SYN Flood Detection
- Denial-of-Service Analysis
- Incident Investigation
- Network Security
- Technical Documentation

---

## Key Takeaways

This exercise reinforced how attackers can exploit the TCP connection establishment process to exhaust server resources.

Understanding TCP behavior is essential for identifying network-based attacks, investigating service outages, and implementing effective defensive measures to maintain system availability.

---

## Supporting Document

The original attack analysis report completed during the Google Cybersecurity Professional Certificate is included in this directory for reference.
