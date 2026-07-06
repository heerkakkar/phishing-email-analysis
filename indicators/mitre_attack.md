# MITRE ATT&CK Mapping

## Objective

This document maps the observed phishing techniques to the MITRE ATT&CK framework.

---

## ATT&CK Techniques

| Technique ID | Technique | Evidence |
|-------------|-----------|----------|
| T1566.002 | Phishing: Spearphishing Link | Email contains a phishing link directing the victim to a fake cloud page |
| T1583.001 | Acquire Infrastructure: Domains | Multiple attacker-controlled domains (`tepyf.kuk`, `solarnodesys.biz.ua`) |
| T1583.003 | Acquire Infrastructure: Virtual Private Server | Email sent from a hosted data center IP (`85.121.55.246`) |
| T1584.001 | Compromise Infrastructure | Use of legitimate cloud infrastructure (Google Cloud Storage) to host phishing content |
| T1036 | Masquerading | Email imitates a legitimate cloud storage service |
| T1204.001 | User Execution: Malicious Link | Victim is encouraged to click the embedded "Update Payment & Secure My Data" button |

---

## Social Engineering Techniques

The phishing campaign used several psychological manipulation methods:

- Urgency ("FINAL NOTICE")
- Fear (Cloud files will be deleted)
- Financial pressure (Payment method expired)
- Trust exploitation ("This message was sent from a trusted sender")
- Brand impersonation (Generic cloud storage service)

---

## ATT&CK Tactics

| Tactic | Purpose |
|---------|---------|
| Initial Access | Deliver phishing email |
| Resource Development | Register attacker domains and infrastructure |
| Defense Evasion | Abuse trusted Google Cloud Storage hosting |
| Credential Access | Direct victim to credential harvesting page |

---

## Assessment

The phishing email aligns closely with the MITRE ATT&CK framework, demonstrating common attacker behaviors used to deliver phishing campaigns and deceive recipients through trusted infrastructure and social engineering.