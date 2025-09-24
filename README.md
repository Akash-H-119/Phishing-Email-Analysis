# Phishing Email Analysis


## Contents
- `Phishing_Email_Analysis_Report.md` – Detailed report of the phishing email analysis.
- `README.md` – short explanation of task & tools used.
- `Visible_details.txt` - Details of the emails.
- `attachment_analysis` - Attachments found in the email.
- `content_findings.md` - Contents found in the email.(urgent language,spoofed sender,suspicious url).
- `header_analysis.txt` - Header Analysis report.
- `headers.txt` - Contains headers of the emails.
- `links_analysis.md` - URL analysis of the emails.
- `Phishing Email Samples` - Email Samples(sample-1.eml,sample-2.eml).

## Tools used

- **MxToolbox Header Analyzer** – for parsing headers (SPF, DKIM, DMARC).
- **EML Analyzer** - for analysing the header(from,to,return_path etc). 
- **VirusTotal** – for checking suspicious links.  
- **Email client (.eml)** – for extracting raw headers.  
- **Manual inspection** – for social engineering traits (urgency, spoofing, etc.).  


## Steps Performed
1. Obtained a sample phishing email.
2. Inspected email headers using an online header analyzer.
3. Identified:
   - Spoofed sender domain.
   - SPF, DKIM, DMARC failures.
   - Suspicious, urgent language.
   - Malicious URL: `https://blog1seguimentmydomaine2bra.me/`.
4. Documented all indicators and attached screenshots.

## Outcome
Developed awareness of phishing tactics, header analysis, and email threat detection.

