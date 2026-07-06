# Phishing Alert Investigation

## Overview

This lab simulates the investigation of a phishing-related security alert in a Security Operations Center (SOC) environment.

The objective was to analyze the alert, identify indicators of compromise (IOCs), assess the potential impact, and determine the appropriate response based on the available evidence.

---

## Objective

- Analyze a phishing-related security alert.
- Examine suspicious email characteristics.
- Identify indicators of compromise (IOCs).
- Assess alert severity.
- Decide whether the incident should be closed or escalated.

---

## Scenario

A security monitoring system generated an alert indicating that an employee may have downloaded and executed a malicious attachment received through a phishing email.

The investigation involved reviewing:

- Alert details
- Email metadata
- Sender information
- Attachment characteristics
- Known malicious file hash
- Overall incident context

---

## Security Concepts

- Security Operations Center (SOC)
- Phishing Detection
- Incident Response
- Alert Triage
- Indicators of Compromise (IOCs)
- Malware Analysis
- Email Security
- Threat Escalation

---

## Investigation Findings

During the investigation, several suspicious indicators were identified:

- Sender email address did not match the displayed sender name.
- The email contained grammatical and formatting errors.
- A password-protected executable attachment was included.
- The attachment matched a known malicious file hash.
- The employee downloaded and executed the attachment.
- The alert was classified as **Medium Severity**.

---

## Indicators of Compromise (IOCs)

The following indicators contributed to the investigation:

- Suspicious sender identity
- Mismatched email address
- Password-protected executable attachment
- Known malicious SHA-256 hash
- Social engineering techniques
- Evidence of user interaction with the attachment

---

## Risk Assessment

The investigation indicated a high probability that the workstation had been compromised through a phishing attack.

Potential risks included:

- Malware execution
- Credential theft
- Unauthorized system access
- Lateral movement
- Data exfiltration

Because the endpoint executed a known malicious file, immediate escalation was required.

---

## Response

Based on the available evidence, the alert was **escalated to a Level 2 SOC Analyst** for further investigation and containment.

Additional response actions that would typically follow include:

- Isolating the affected endpoint
- Performing malware analysis
- Blocking malicious indicators
- Resetting compromised credentials
- Reviewing endpoint telemetry
- Conducting a full incident investigation

---

## Skills Demonstrated

- SOC Alert Analysis
- Phishing Investigation
- Email Threat Analysis
- IOC Identification
- Incident Triage
- Security Documentation
- Risk Assessment
- Escalation Decision Making

---

## Key Takeaways

This exercise demonstrated the importance of carefully analyzing phishing alerts before determining the appropriate response.

Multiple indicators—including sender inconsistencies, malicious attachments, known file hashes, and user interaction—provided sufficient evidence to justify escalation for further incident response.

The lab also reinforced the role of a SOC analyst in identifying threats, documenting findings, and ensuring that potentially compromised systems receive timely investigation.

---

## Supporting Document

The completed SOC alert ticket submitted during the Google Cybersecurity Professional Certificate is included in this directory for reference.
