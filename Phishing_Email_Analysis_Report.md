# Phishing Email Analysis Report

## Objective
Analyze a suspicious email to identify phishing indicators and document the findings.

---

## Email Header Summary
| Field        | Observation |
|------------- |------------ |
| **Subject**  | CLIENTE PRIME - BRADESCO LIVELO: Seu cartão tem 92.990 pontos LIVELO expirando hoje! |
| **From**     | banco.bradesco@atendimento.com.br |
| **To**       | phishing@pot |
| **Date**     | 2023-09-19 18:35:49 UTC |
| **Message ID** | <20230919183549.39DEA3F725@ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06> |

---

## Header Security Checks
| Check  | Result       | Reason for Concern |
|--------|-------------|-------------------|
| SPF    | temperror   | Sender IP not authorized to send on behalf of atendimento.com.br |
| DKIM   | none        | Message not cryptographically signed |
| DMARC  | temperror   | Domain owner’s policy not met |

---

## Phishing Indicators
1. **Spoofed Sender Domain**  
   - Appears as `banco.bradesco@atendimento.com.br` but real Bradesco uses `bradesco.com.br`.

2. **Failed Email Authentication**  
   - SPF, DKIM, and DMARC checks all failed.

3. **Urgent Language**  
   - “92.990 points expiring today” pressures immediate action.

4. **Unusual Sending Host**  
   - Message ID shows a generic Ubuntu mail server, not a bank system.

5. **Malicious URL**  
   - Extracted URL: `https://blog1seguimentmydomaine2bra.me/`  
   - This is not an official Bradesco domain and likely hosts a phishing site.

---

## Screenshots
- **Header analysis output** (attach your header screenshot image file).
- **Extracted URL output** (attach your malicious-link screenshot image file).

---

## Conclusion
This email is a classic phishing attempt designed to steal user credentials:
- Spoofed “From” address
- Failed SPF/DKIM/DMARC authentication
- Urgent social-engineering wording
- Malicious redirect link

---

## Recommendations
- Do **not** click any links or open attachments.
- Report the email to your email provider’s abuse or phishing address.
- Educate users about verifying domains and checking email headers.
