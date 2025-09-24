# Phishing Email Analysis Report

## Objective
Analyze suspicious emails to identify phishing indicators and document the findings.

---

# 📧 Email Sample 1 – Bradesco Livelo Points
<img width="786" height="718" alt="image" src="https://github.com/user-attachments/assets/be2299bd-d798-4960-bf55-5d967019b7ed" />


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
- **Header analysis output**.
<img width="1560" height="908" alt="image" src="https://github.com/user-attachments/assets/d3557758-cf93-40f0-8abe-8117920c31c4" />
<img width="1239" height="206" alt="image" src="https://github.com/user-attachments/assets/aff8a5f9-f1dc-4c7c-a3c1-c0323ed0c1c6" />


- **Extracted URL output** .
<img width="1667" height="965" alt="image" src="https://github.com/user-attachments/assets/0d8e9265-4b4a-496f-b571-33110959b3a5" />
- URL: https://blog1seguimentmydomaine2bra.me/
- VirusTotal result: No security vendors flagged this URL as malicious.
- Reason still suspicious:
  - Domain name does not match official Bradesco domain.
  - URL structure looks auto-generated and shady.
  - Came from a spoofed banking email.

- 


---

## Conclusion
This is a phishing attempt targeting bank customers using urgency and a spoofed sender identity.  

---

# 📧 Email Sample 2 – Solar Panels Offer
<img width="507" height="808" alt="image" src="https://github.com/user-attachments/assets/7d949d8a-0c4f-4da5-a4ad-178f4df729df" />

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
- **email header screenshot**.
<img width="1721" height="926" alt="image" src="https://github.com/user-attachments/assets/e6f0dea2-369c-41f7-adc4-db1623856c0e" />
<img width="1454" height="225" alt="image" src="https://github.com/user-attachments/assets/f245df39-713b-429c-8e5e-7a5c040d99a1" />

  
- **email body screenshot** .  

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
