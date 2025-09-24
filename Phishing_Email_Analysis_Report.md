# Phishing Email Analysis Report

## Objective
Analyze suspicious emails to identify phishing indicators and document the findings.

---

# 📧 Email Sample 1 – Bradesco Livelo Points

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
| SPF    | temperror   | Sender IP not authorized for atendimento.com.br |
| DKIM   | none        | Message not cryptographically signed |
| DMARC  | temperror   | Domain owner’s policy not met |

---

## Phishing Indicators
1. **Spoofed Sender Domain**  
   - Appears as `banco.bradesco@atendimento.com.br`, but real Bradesco uses `bradesco.com.br`.  

2. **Failed Email Authentication**  
   - SPF, DKIM, and DMARC checks all failed.  

3. **Urgent Language**  
   - “92.990 points expiring today” pressures immediate action.  

4. **Unusual Sending Host**  
   - Message ID shows a generic Ubuntu mail server, not a Bradesco server.  

5. **Malicious URL**  
   - Extracted: `https://blog1seguimentmydomaine2bra.me/`  
   - Clearly not an official Bradesco domain.  

---

## Screenshots
- **Header analysis output** (attach screenshot).  
- **Extracted URL output** (attach screenshot).  

---

## Conclusion
This is a phishing attempt targeting bank customers using urgency and a spoofed sender identity.  

---

# 📧 Email Sample 2 – Solar Panels Offer

## Email Header Summary
| Field        | Observation |
|------------- |------------ |
| **Subject**  | Zonnepanelen voor een goede prijs (Solar panels for a good price) |
| **From**     | zonnepaneel@appjj.serenitepure.fr |
| **To**       | phishing@pot… |
| **Date**     | 2022-11-03 04:56:15 UTC |
| **Message ID** | <0.0.0.0.1D8EF409A5C12CE.37AA@dturn.de> |

---

## Header Security Checks
| Check  | Result | Reason for Concern |
|--------|--------|-------------------|
| SPF    | none   | Sender IP (57.128.69.202) not authorized |
| DKIM   | none   | Message not cryptographically signed |
| DMARC  | none   | No policy applied |

---

## Phishing Indicators
1. **Spoofed Sender Domain**  
   - `@serenitepure.fr` domain unrelated to solar panel offers.  

2. **Failed Authentication**  
   - SPF, DKIM, and DMARC all failed.  

3. **Suspicious Routing**  
   - Sent via `dturn.de` server, not aligned with sender domain.  

4. **Marketing Bait**  
   - Subject promises “a good price” to lure clicks.  

---

## Screenshots
- Add **email header screenshot** (from header analyzer).  
- Add **email body screenshot** if available.  

---

## Conclusion
This is a phishing attempt using a spoofed domain and failed authentication checks to deliver a marketing-style lure.  

---

# ✅ Overall Recommendations
- Do **not** click links or open attachments in suspicious emails.  
- Always verify sender domains against official ones.  
- Check email headers for SPF/DKIM/DMARC failures.  
- Educate users about common phishing tactics.  
- Report phishing to abuse teams or security contacts.  
