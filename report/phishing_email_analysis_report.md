# Phishing Email Analysis Report

## Case Information

| Field | Value |
|--------|-------|
| Analyst | Heer Kakkar |
| Analysis Date | 06 July 2026 |
| Case ID | PE-2026-001 |
| Investigation Type | Phishing Email Investigation |
| Evidence | Suspicious phishing email exported as `.eml` |

---

# Executive Summary

A suspicious email claiming that the recipient's cloud files would be permanently deleted within 24 hours was investigated. The email employed urgency, fear, and impersonation techniques to convince the recipient to click a malicious link hosted on Google Cloud Storage. Although SPF and DKIM authentication checks passed, DMARC validation failed due to domain misalignment, indicating possible sender spoofing. Threat intelligence analysis identified the sending IP as a hosted data center server with previous phishing reports. Based on the collected evidence, the email has been classified as a high-confidence phishing attempt.

---

# Investigation Scope

This investigation includes:

- Email Header Analysis
- Sender Verification
- Email Authentication Analysis (SPF, DKIM, DMARC)
- URL Analysis
- Domain Analysis
- IP Reputation Analysis
- Social Engineering Analysis
- IOC Extraction
- Risk Assessment

---

# Investigation Methodology

1. Initial Email Triage
2. Header Analysis
3. Sender Analysis
4. Authentication Analysis
5. URL Investigation
6. Domain Investigation
7. IP Reputation Analysis
8. Social Engineering Analysis
9. IOC Extraction
10. Final Verdict

---

# Findings

## 1. Email Header Analysis

> See `analysis/02_header_analysis.md`

---

## 2. Sender Analysis

> See `analysis/03_sender_analysis.md`

---

## 3. Authentication Analysis

> See `analysis/04_authentication_analysis.md`

---

## 4. URL Analysis

> See `analysis/05_url_analysis.md`

---

## 5. Domain Analysis

> See `analysis/07_domain_analysis.md`

---

## 6. IP Reputation Analysis

> See `analysis/06_ip_analysis.md`

---

## 7. Social Engineering Analysis

> See `analysis/08_social_engineering_analysis.md`

---

# Indicators of Compromise (IOCs)

> See `indicators/iocs.md`

---

# MITRE ATT&CK Mapping

> See `indicators/mitre_attack.md`

---

# Risk Assessment

| Category | Result |
|----------|--------|
| Classification | Phishing Email |
| Severity | High |
| Confidence | High |

---

# Recommendations

- Do not click links or download attachments from suspicious emails.
- Verify the sender's identity before responding to urgent requests.
- Reject emails that fail DMARC authentication where appropriate.
- Block identified malicious domains and IP addresses in email security solutions.
- Monitor for similar Indicators of Compromise (IOCs) across the environment.
- Educate users on common phishing techniques such as urgency, impersonation, and fear-based social engineering.

---

# Conclusion

The investigation confirmed that the email is a phishing attempt designed to trick recipients into visiting a fraudulent payment page through a malicious link hosted on Google Cloud Storage. The attacker used multiple domains, social engineering tactics, and trusted cloud infrastructure to increase credibility. Although SPF and DKIM checks passed, the failed DMARC validation, suspicious sender domains, malicious infrastructure, and phishing-themed content strongly indicate malicious intent. Users should avoid interacting with the email and report similar messages to their security team.

---

# References

- VirusTotal
- URLScan.io
- AbuseIPDB
- WHOIS
- Google Message Header Analyzer

---

# Disclaimer

This report was prepared for educational and portfolio purposes. Personally identifiable information (PII) has been redacted to protect privacy. All findings are based on evidence collected during the investigation and reflect observations made at the time of analysis.