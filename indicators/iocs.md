# Indicators of Compromise (IOCs)

## Objective

This document lists the Indicators of Compromise (IOCs) extracted during the phishing email investigation. These indicators can be used by security teams to detect, investigate, and block similar attacks.

---

## Email Indicators

| Type | Indicator |
|------|-----------|
| Subject | FINAL NOTICE: Your cloud files will be deleted within 24 hours |
| Message-ID | `<alert-4712@tepyf.kuk>` |
| From Domain | `tepyf.kuk` |
| Return-Path Domain | `store.bss0010.solarnodesys.biz.ua` |
| DKIM Domain | `wwEr.store.bss0010.solarnodesys.biz.ua` |

---

## Network Indicators

| Type | Indicator |
|------|-----------|
| Sending IP | `85.121.55.246` |
| Sending Host | `store.bss0010.solarnodesys.biz.ua` |
| Receiving Mail Server | `mx.google.com` |

---

## URL Indicators

| URL | Purpose |
|-----|---------|
| `https://storage.googleapis.com/hmdbox/hmd-v1-cl2.html` | Credential harvesting page |
| `https://storage.googleapis.com/hmdbox/hmd-v1-cl2.html#...` | Unsubscribe / tracking link |

---

## Authentication Results

| Mechanism | Result |
|-----------|--------|
| SPF | PASS |
| DKIM | PASS |
| DMARC | FAIL |

---

## Threat Intelligence Summary

- Hosting platform: Google Cloud Storage
- URL detections (VirusTotal): **5 / 92**
- AbuseIPDB reports: **5**
- Hosting Type: Data Center
- IP Country: Netherlands

---

## Detection Opportunities

Security teams can create detection rules based on:

- Sender domain (`tepyf.kuk`)
- Sending IP (`85.121.55.246`)
- DKIM domain (`wwEr.store.bss0010.solarnodesys.biz.ua`)
- Google Cloud Storage phishing URL
- DMARC authentication failure

---

## Conclusion

The extracted indicators provide multiple opportunities for email filtering, threat hunting, and incident response. Organizations should monitor these IOCs and update detection rules where appropriate.