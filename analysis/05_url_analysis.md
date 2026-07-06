# URL Analysis

## Objective

The objective of this phase is to analyze all URLs embedded in the email to determine whether they lead to malicious, suspicious, or legitimate destinations. This includes checking domain reputation, hosting infrastructure, redirection behavior, and security indicators.

---

## Extracted URL(s)

- `https://storage.googleapis.com/...` *(Google Cloud Storage link observed in email content)*

---

## URL Overview

| Attribute | Value |
|----------|------|
| Domain | storage.googleapis.com |
| Hosting Provider | Google LLC |
| Infrastructure Type | Cloud Storage |
| HTTPS | Enabled |
| URL Shortener | No |

---

## Reputation Analysis

- The domain `storage.googleapis.com` is a legitimate Google-owned service.
- The infrastructure is widely used for hosting files, including static web content.
- However, legitimate hosting does NOT guarantee safety of content stored within it.

Security tools observed:
- urlscan.io: No malicious classification
- Google Safe Browsing: No classification
- Multiple scans performed on same domain (high usage frequency)
## VirusTotal Analysis
The URL was analyzed using VirusTotal and received a score of **5/92 detections**.
This indicates that while the majority of security vendors did not classify the URL as malicious, a small number of engines flagged it as suspicious or potentially harmful.
This discrepancy suggests that the URL should not be considered fully safe and requires further contextual analysis.

---

## Security Interpretation

Although the URL is hosted on legitimate Google Cloud infrastructure (`storage.googleapis.com`), VirusTotal detections indicate potential malicious activity associated with the content hosted on the URL.

This highlights a common phishing technique where attackers abuse trusted cloud services to bypass reputation-based security filters.

Therefore, the reputation of the hosting domain alone is not sufficient to classify the URL as safe.

---

## Key Observations

- The URL uses trusted infrastructure (Google Cloud Storage), which can help attackers bypass basic reputation filters.
- The actual content hosted on the URL is not controlled by Google, only the storage service is.
- Attackers commonly abuse cloud storage platforms to host phishing pages due to their trusted reputation.
- No URL shorteners were used, which slightly increases transparency but does not guarantee safety.

---

## Risk Indicators

| Indicator | Status | Explanation |
|-----------|--------|-------------|
| Trusted Domain | ✅ Yes | Google-owned infrastructure |
| Malicious Classification | ❌ No | No direct detection by tools |
| Hidden Redirects | ⚠️ Unknown | Requires deeper inspection |
| Phishing Risk | ⚠️ Medium | Trusted hosting can still be abused |

---

## Security Interpretation

Although the URL is hosted on a legitimate domain (`storage.googleapis.com`), this does not guarantee safety. Cloud storage services are frequently used in phishing campaigns to host:

- Fake login pages
- Credential harvesting forms
- Redirect scripts

Therefore, URL reputation alone is insufficient for classification. Content analysis is required.

---

## Preliminary Conclusion

The URL does not appear malicious based on domain reputation, but the use of cloud infrastructure introduces moderate risk due to potential abuse for phishing content hosting.

Further analysis is required in:
- IP reputation analysis
- Content inspection (if accessible)
- Behavior analysis of landing page

---

