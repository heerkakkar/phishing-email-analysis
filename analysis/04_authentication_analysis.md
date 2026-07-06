# Email Authentication Analysis (SPF, DKIM, DMARC)

## Objective

The objective of this phase is to verify the authenticity of the email using standard email authentication mechanisms:
- SPF (Sender Policy Framework)
- DKIM (DomainKeys Identified Mail)
- DMARC (Domain-based Message Authentication, Reporting & Conformance)

These checks help determine whether the email was legitimately sent from the claimed domain or if it was spoofed.

---

## Authentication Summary

| Mechanism | Result | Evidence |
|-----------|--------|----------|
| SPF | PASS | IP: 85.121.55.246 authorized |
| DKIM | PASS | Signed by `wwEr.store.bss0010.solarnodesys.biz.ua` |
| DMARC | FAIL | Alignment check failed |

---

## SPF Analysis

**Result:** PASS

The SPF check passed, indicating that the sending IP address `85.121.55.246` is authorized to send emails for the domain used in SPF validation.

However, SPF only validates the sending server, not the legitimacy of the message content or sender identity.

---

## DKIM Analysis

**Result:** PASS

The email passed DKIM verification using the domain:

`wwEr.store.bss0010.solarnodesys.biz.ua`

This confirms that the email content was not altered during transit.

However, DKIM does not guarantee that the domain itself is trustworthy or related to a legitimate organization.

---

## DMARC Analysis

**Result:** FAIL

The email failed DMARC authentication.

DMARC failure indicates that the email did not pass domain alignment checks between:
- SPF domain
- DKIM signing domain
- Visible "From" domain

Why DMARC failed

Visible From: tepyf.kuk
SPF domain: store.bss0010.solarnodesys.biz.ua
DKIM domain: wwEr.store.bss0010.solarnodesys.biz.ua

These domains are not aligned, so DMARC fails.
Even though SPF and DKIM passed individually, they are not aligned with the displayed sender identity, leading to DMARC failure.

This is a strong indicator of potential phishing activity.

---

## Key Observations

- SPF and DKIM both passed, indicating technically valid sending infrastructure.
- DMARC failed due to lack of alignment with the visible sender domain.
- The DKIM signing domain does not match the display sender domain.
- This mismatch is commonly observed in phishing campaigns using domain impersonation techniques.

---

## Security Interpretation

| Factor | Interpretation |
|--------|---------------|
| SPF PASS | Server allowed to send email |
| DKIM PASS | Message integrity maintained |
| DMARC FAIL | Identity mismatch detected |

The combination of SPF PASS + DKIM PASS + DMARC FAIL suggests that while the email was technically sent through valid infrastructure, the identity alignment is suspicious and inconsistent with legitimate communication patterns.

---

## Preliminary Conclusion

Authentication results indicate that the email passed individual validation checks but failed alignment verification. This strongly suggests possible domain impersonation or misuse of authorized sending infrastructure.

Further validation is required using:
- URL analysis
- Domain reputation checks
- IP reputation analysis

---

