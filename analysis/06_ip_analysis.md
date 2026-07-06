# IP Reputation Analysis

## Objective

The objective of this phase is to analyze the sending IP address to determine its reputation, hosting behavior, geographic location, and any historical abuse reports associated with it. This helps identify whether the infrastructure is associated with malicious activity.

---

## Analyzed IP Address

- **IP Address:** `85.121.55.246`

---

## IP Overview

| Attribute | Value |
|----------|------|
| ISP | Urban Network Solutions SRL |
| ASN | AS9009 |
| Hosting Type | Data Center / Web Hosting |
| Country | Netherlands 🇳🇱 |
| City | The Hague |
| Hostname | ampglobal.tdsynnex.com |

---

## Reputation Analysis

The IP address was analyzed using multiple threat intelligence sources.

### Abuse Reports

- IP has been reported **5 times**
- Confidence of abuse: **Low (2%)**
- Report categories include:
  - Spam emails
  - Phishing attempts
  - Spoofed sender activity

---

## Key Observations

- The IP belongs to a **data center hosting provider**, not a residential ISP.
- Data center IPs are commonly used for:
  - Bulk email sending
  - Automated scripts
  - Phishing infrastructure
- The IP has a **history of spam/phishing reports**, indicating prior malicious usage.
- Low abuse confidence does not mean safe — it only reflects limited reporting.

---

## Geolocation Note

Although IP geolocation shows **Netherlands**, earlier checks may show different country results (e.g., United States).

### Explanation:
- IP geolocation databases are not always consistent.
- Large providers like Google or hosting companies use:
  - Load balancing
  - Anycast routing
  - Distributed infrastructure

👉 Therefore, IP location should be considered **approximate, not absolute**.

---

## Security Interpretation

| Factor | Assessment |
|--------|-----------|
| Hosting Type | ⚠️ Suspicious (Data Center) |
| Abuse History | ⚠️ Some reports present |
| ISP Reputation | ⚠️ Neutral to low trust |
| Residential IP | ❌ No |

The use of a data center IP with prior abuse reports increases the likelihood that the infrastructure may be associated with automated or malicious email activity.

---

## Preliminary Conclusion

The sending IP `85.121.55.246` is not directly confirmed as malicious, but multiple indicators suggest elevated risk:

- Data center hosting environment
- Previous abuse reports (spam/phishing)
- Use in automated email delivery infrastructure

This IP should be considered **suspicious and untrusted for email origin verification**.

---

## Next Step

