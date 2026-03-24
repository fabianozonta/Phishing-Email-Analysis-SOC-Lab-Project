# Phishing Email Analysis – SOC Lab Project

## Overview

This project documents the analysis of a real phishing email using a structured SOC methodology.

The goal was to simulate how a Security Operations Center (SOC) would investigate a suspected phishing attempt from detection through classification and response planning.

---

## Objectives

* Perform full email header analysis
* Validate SPF, DKIM, and DMARC results
* Identify malicious infrastructure
* Extract Indicators of Compromise (IoCs)
* Map activity to MITRE ATT&CK
* Develop an incident response runbook

---

## Scenario Summary

A phishing email impersonating trusted organizations was identified in a spam folder. The message encouraged the recipient to verify billing information via a malicious link.

Although SPF, DKIM, and DMARC passed, the sender domain was newly registered and unrelated to the impersonated brands.

This demonstrates a modern phishing technique using properly configured email authentication to bypass basic security checks.

---

## Key Findings

* Domain used: follaljazeerah.com
* Email authentication: SPF/DKIM/DMARC passed
* Delivery path: Sent via legitimate mail relay
* Attack type: Brand impersonation
* Likely objective: Credential harvesting

---

## MITRE ATT&CK Mapping

* T1566.002 – Phishing: Link
* T1583 – Acquire Infrastructure
* T1598 – Phishing for Information

---

## Extracted Indicators of Compromise

* Sender email
* Sending IP address
* Malicious domain
* Embedded URL

---

## Incident Response Actions Proposed

* Block domain at gateway and DNS layer
* Conduct SIEM search for additional recipients
* Investigate potential user clicks
* Reset credentials if exposure confirmed

---

## Skills Demonstrated

* Email header forensic analysis
* Threat classification
* IOC extraction
* Incident documentation
* SOC workflow simulation

---

## Conclusion

This project reinforces the importance of contextual analysis in phishing detection. Technical authentication alone is not sufficient to determine legitimacy.

Structured investigation and documentation are critical components of effective SOC operations.

End of project documentation.
