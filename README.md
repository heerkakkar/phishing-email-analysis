# 📧 Phishing Email Analysis

> A hands-on phishing email investigation performed using real-world email analysis techniques and open-source intelligence (OSINT) tools.

## 📌 Project Overview

This project documents the investigation of a suspicious email that was exported from an email client as an .eml file. The analysis aims to determine whether the email is legitimate or malicious by examining its headers, sender information, authentication records, embedded URLs, domains, and other Indicators of Compromise (IOCs).

The investigation follows a structured methodology similar to the workflow used by Security Operations Center (SOC) analysts.

---

## 🎯 Objectives

- Perform an initial triage of a suspicious email.
- Analyze email headers and metadata.
- Verify sender authenticity using SPF, DKIM, and DMARC.
- Identify social engineering techniques used to manipulate the      recipient.
- Investigate embedded URLs using OSINT tools.
- Analyze domains and IP addresses associated with the email.
- Extract and document Indicators of Compromise (IOCs).
- Map observed techniques to the MITRE ATT&CK framework.
- Assess the overall risk and provide an evidence-based verdict.

NOTE:
This .eml file is a sanitized version of the original phishing email.
Personally identifiable information (PII), tracking parameters, and
non-essential data have been redacted to protect privacy while preserving
the technical artifacts required for forensic analysis.

---

## 🔬 Investigation Methodology

The investigation follows these phases:

1. Initial Email Triage
2. Email Header Analysis
3. Sender Verification
4. Email Authentication Analysis (SPF, DKIM, DMARC)
5. URL Investigation
6. Domain Analysis
7. IP Reputation Analysis
8. Social Engineering Analysis
9. IOC Extraction
10. Risk Assessment & Final Verdict


---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Google Message Header Analyzer | Analyze email headers |
| MXToolbox | SPF, DKIM, DMARC validation |
| VirusTotal | Domain, IP, and URL reputation |
| URLScan.io | URL behavior analysis |
| WHOIS | Domain registration lookup |
| AbuseIPDB | IP reputation analysis |

---

## 📂 Repository Structure

phishing email analysis/
│
├── README.md
├── LICENSE
│
├── report/
│   └── phishing_email_analysis_report.md
│
├── analysis/
│   ├── 01_initial_triage.md
│   ├── 02_header_analysis.md
│   ├── 03_sender_analysis.md
│   ├── 04_authentication_analysis.md
│   ├── 05_url_analysis.md
│   ├── 06_ip_analysis.md
│   ├── 07_domain_analysis.md
│   └── 08_social_engineering_analysis.md
│
├── evidence/
│   ├── suspicious_email.eml
│   ├── extracted_headers.txt
│   └── screenshots/
        
│
├── indicators/
│   ├── iocs.md
│   └── mitre_attack.md

```

---

## 📁 Evidence

The investigation is based on the original email exported as an `.eml` file, preserving the complete email, including:

- Email headers
- Message metadata
- HTML content
- Embedded URLs
- MIME structure

This enables a forensic analysis while maintaining the integrity of the original email.

---

## 🔒 Privacy Notice

Some information in this repository has been **redacted** to protect personal privacy and prevent misuse. Redacted items may include email addresses, recipient information, and other personally identifiable information (PII). The technical findings and conclusions remain unchanged.



## ⚠️ Disclaimer

This repository was created for **educational and portfolio purposes**. Any domains, IP addresses, email addresses, or URLs included are documented solely for security analysis and research. Their presence in this repository does **not** imply current malicious activity, and findings reflect observations made during the time of investigation.

---

## 📖 References

- RFC 5322 – Internet Message Format
- MITRE ATT&CK Framework
- VirusTotal
- URLScan.io
- AbuseIPDB
- MXToolbox

---

## 👨‍💻 Author

**Heer Kakkar**

Cybersecurity Student | SOC Analyst Aspirant | Ethical Hacking Enthusias