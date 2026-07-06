# Email Header Analysis

## Objective

The objective of this phase was to examine the email headers to determine the true origin of the message, verify the sender's identity, analyze the delivery path, and identify technical indicators that may suggest phishing or malicious activity.

---

## What are Email Headers?

Email headers contain metadata about an email, including the sender, recipient, mail servers involved in delivery, authentication results, timestamps, and routing information. Unlike the visible email content, headers provide technical evidence that helps analysts verify the legitimacy of an email.

---

## Header Fields Examined

| Header Field | Purpose |
|--------------|---------|
| From | Displays the sender's email address shown to the recipient. |
| Return-Path | Indicates where bounced emails are returned. |
| Reply-To | Specifies the address that receives replies. |
| Received | Records the route taken by the email through mail servers. |
| Message-ID | Unique identifier assigned to the email. |
| MIME-Version | Specifies the MIME format used. |
| Content-Type | Indicates whether the email contains HTML, plain text, or attachments. |
| SPF | Verifies whether the sending server is authorized. |
| DKIM | Verifies the digital signature of the email. |
| DMARC | Defines how SPF and DKIM results are evaluated. |

---

## Header Summary

| Field | Observation |
|--------|-------------|
| Subject | 🚨 FINAL NOTICE: Your cloud files will be deleted within 24 hours |
| Email Format | `.eml` |
| Message-ID | <alert-4712@tepyf.kuk> |
| MIME Version | 1.0 |
| Content Type | HTML Email *(update with your actual value)* |

---

## Email Routing

The **Received** headers were examined to trace the path of the email from the sending mail server to the recipient.

### Originating Mail Server

- IP Address: `85.121.55.246`
- Geolocation: Netherlands
- ISP: Urban Network Solutions SRL

The sending IP was extracted for further reputation analysis using AbuseIPDB and IP information lookup services.

---

## Authentication Summary

| Authentication | Result |
|----------------|--------|
| SPF | PASS |
| DKIM | PASS |
| DMARC | FAIL |

Passing authentication checks indicates that the sending server was authorized for the sender's domain and that the email contents were not modified during transit. However, successful authentication alone does not guarantee that an email is legitimate, as attackers can configure these mechanisms for domains under their control.
### DMARC Analysis

The email failed the DMARC authentication check. DMARC verifies whether the sender's domain aligns with the results of SPF and/or DKIM.

A DMARC failure indicates that the email did not satisfy the domain alignment requirements defined by the sender's DMARC policy. While a DMARC failure alone does not confirm phishing, it is a significant indicator that the email requires further investigation.

---

## Key Observations

- The email was successfully delivered through authenticated mail servers.
- The sending infrastructure was identified for further OSINT investigation.
- Header information was preserved through the exported `.eml` file.
- Additional investigation of URLs, domains, and IP reputation was required before determining whether the email was malicious.

---

## Next Step

The next phase focuses on verifying the sender's identity and examining whether the sender information is consistent throughout the email.