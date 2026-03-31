# Phishing-email-incident-response-
SOC investigation of a phishing email that delivered a malicious executable attachment. The project demonstrates alert triage, malware hash verification, and incident escalation workflow.



# SOC Phishing & Malware Incident Investigation

## Overview

This project documents the investigation of a phishing email alert that indicated a potential malware download. The alert originated from a monitored mail server and suggested that a user may have opened a malicious email and executed an attachment.

The purpose of this investigation was to analyze the alert details, identify phishing indicators, verify the malicious file hash, and determine the appropriate escalation procedure.

---

## Alert Ticket Information

| Field | Value |
|------|------|
| Ticket ID | A-2703 |
| Alert Source | SERVER-MAIL |
| Alert Type | Phishing Attempt / Possible Malware Download |
| Severity | Medium |
| Ticket Status | Escalated |

The alert indicated that the user may have opened a malicious email and interacted with an attachment or link.

---

## Ticket Comments

The investigation revealed several suspicious indicators associated with the email and attachment.

- The file contained malicious links that redirected users to external websites.
- The file executed malicious code on the employee's computer.
- The email contained grammatical errors, which is a common indicator of phishing.
- The email subject and body contained multiple spelling and grammar mistakes.
- The email included a password-protected attachment named **bfsvc.exe**.

The attachment was downloaded and opened on the affected machine. After investigating the file hash, it was confirmed to be a **known malicious file**.

Based on these findings and the alert severity level, the incident was escalated to a **Level 2 SOC analyst** for further investigation and response.

---

## Email Information

**Sender** 
IP: 114.114.114.114

**Recipient**
IP: 176.157.125.93


**Date**
Wednesday, July 20, 2022 09:30:14 AM


**Subject**
Re: Infrastructure Egnieer role
---
## Suspicious Email Content

Example excerpt from the email:

> Dear HR at Ingergy,  
> I am writing for to express my interest in the engineer role posted from the website.  
> There is attached my resume and cover letter. For privacy, the file is password protected. Use the password paradise10789 to open.

The message contained several indicators of phishing, including grammatical errors and a suspicious password-protected attachment.

---

## Malicious Attachment
Filename: bfsvc.exe

The attachment was downloaded and opened on the employee's system.

After investigation, the file hash was confirmed to match a known malicious file.

**SHA256 Hash**
54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b


---

## Indicators of Compromise (IOCs)

| Indicator Type | Value |
|---------------|------|
| File Name | bfsvc.exe |
| SHA256 Hash | 54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b |
| Sender IP | 114.114.114.114 |
| Recipient IP | 176.157.125.93 |

These indicators can be used to detect similar malicious activity within security monitoring tools such as SIEM or endpoint protection systems.

---

