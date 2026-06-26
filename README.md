# Phishing Email Investigation

## Overview

This repository documents the investigation of a phishing email that impersonates a philanthropist offering a **$10.5 million donation** to randomly selected individuals. The investigation focuses on analyzing the email header, authentication results, sender information, routing path, and message content to determine whether the email is legitimate or malicious.

The analysis follows a structured SOC analyst methodology and demonstrates how multiple technical and behavioral indicators can be combined to identify phishing attempts.

---

## Objectives

* Analyze email header information
* Verify sender identity
* Examine SPF, DKIM, and DMARC authentication
* Trace the email delivery path
* Identify social engineering techniques
* Determine the legitimacy of the email
* Document findings in a structured investigation report

---

## Repository Structure

```
Phishing-Email-Investigation/
│
├── README.md
│
├── Email/
│   └──phishing_Email.txt
|   └──sample-1004.eml
│
└── Analysis_Report/
|    └── Phishing_Email_Analysis.docx
|
├──Screenshots
```

---

## Investigation Methodology

The investigation was conducted using the following approach:

1. Reviewed the email header.
2. Examined the sender, Reply-To, and Return-Path fields.
3. Verified SPF, DKIM, and DMARC authentication results.
4. Traced the email's delivery route using the Received headers.
5. Analyzed the email content for social engineering techniques.
6. Identified indicators of compromise (IOCs).
7. Reached a final assessment based on technical and behavioral evidence.

---

## Key Findings

* Display name does not match the sender's email address.
* Different Reply-To address redirects responses to a Gmail account.
* SPF authentication returned **SoftFail**.
* No DKIM signature was present.
* DMARC authentication failed and recommended quarantine.
* The email originated from an untrusted mail server.
* The message promises an unrealistic **$10.5 million donation**.
* The email was sent to **Undisclosed recipients**, indicating a bulk mailing campaign.
* The message relies on social engineering techniques to encourage the recipient to respond.

---

## Skills Demonstrated

* Email Header Analysis
* Email Authentication Analysis (SPF, DKIM, DMARC)
* Email Routing Analysis
* Phishing Detection
* Social Engineering Analysis
* Indicator of Compromise (IOC) Identification
* Security Incident Documentation
* Technical Report Writing

---

## Final Verdict

Based on the header analysis, authentication failures, sender inconsistencies, email routing information, and social engineering indicators, this email was classified as a **High-Confidence Phishing Email**.

---

## Disclaimer

The phishing email sample analyzed in this repository was obtained from a publicly available source and is used solely for educational and cybersecurity research purposes. The purpose of this project is to demonstrate practical phishing email analysis techniques and SOC investigation methodology.
