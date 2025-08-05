# 🕵️‍♂️ Phishing Email Analysis - Task 2

This project demonstrates how to analyze a suspicious email sample to identify phishing characteristics. The analysis involves:

- 📧 Examining the sender's email address for spoofing  
- 🔍 Checking email headers for inconsistencies using free online header analyzers  
- 🔗 Identifying suspicious links and attachments  
- ⚠️ Detecting urgent or threatening language within the email body  
- 🖱️ Verifying mismatched URLs by hovering over links  
- ✍️ Spotting spelling and grammar errors  

The final deliverable is a report that lists all phishing indicators found in the sample email, helping users recognize and protect against phishing attacks.

# 🛡️ Phishing Email Analysis: Bradesco Livelo Scam

This repository presents an in-depth analysis of a phishing email that impersonates **Banco Bradesco** and falsely claims the recipient has **92,990 Livelo points expiring today**. The analysis follows a systematic approach to identifying typical phishing indicators.

---
![image of email](https://github.com/shindeharsh3399/Task-2-Analyze-a-Phishing-Email-Sample/blob/main/Screenshot%202025-08-05%20184438.png)

---
## 🧾 1. Sample Phishing Email

- **File:** [BRADESCO LIVELO.eml](https://github.com/shindeharsh3399/Task-2-Analyze-a-Phishing-Email-Sample/blob/main/BRADESCO%20LIVELO.eml)
- **Subject:** `CLIENTE PRIME - BRADESCO LIVELO: Seu cartão tem 92.990 pontos LIVELO expirando hoje!`
- **Claim:** The email urges the recipient to redeem expiring reward points immediately.
- **Purpose:** Trick the user into clicking a malicious link and likely submitting personal/financial data.

---

## 🔍 2. Sender Address Examination

- **From Address:** `banco.bradesco@atendimento.com.br`
- **Analysis:** The domain name does not match Bradesco's official communication channels. It is likely **spoofed** to appear legitimate.

---

## 🧾 3. Email Header Analysis

- **Tool Used:** [Google Admin Toolbox Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/)
- **Findings:**
  - **SPF:** TempError – DNS timeout
  - **DKIM:** Not signed
  - **DMARC:** TempError – validation failed
  - **Authentication-Results:** `compauth=fail`

These failures suggest the sender is **unauthorized and unverified**, increasing suspicion.
 
---
![image of header analyzer](https://github.com/shindeharsh3399/Task-2-Analyze-a-Phishing-Email-Sample/blob/main/Screenshot%202025-08-05%20194207.png)

---

## 🔗 4. Suspicious Links/Attachments

- **Link Found:** A button labeled *"Resgatar Agora"* (Redeem Now)
- **Destination:** Obfuscated with a suspicious, non-Bradesco domain (e.g., `https://blog1seguimentmydomaine2bra[.]me`)
- **Danger:** Clicking may redirect to a credential-harvesting site or deliver malware

> ⚠️ **No attachments were found**, but the malicious link is the primary threat.

![image of links](https://github.com/shindeharsh3399/Task-2-Analyze-a-Phishing-Email-Sample/blob/main/Screenshot%202025-08-05%20190229.png)

---

## ⏰ 5. Urgent or Threatening Language

- **Example:** “Seu cartão tem **92.990 pontos expirando hoje!**”
- **Intent:** Create panic and push the user to act immediately without verifying authenticity.

---

## 🔀 6. Mismatched URLs

- **Displayed Text:** Suggests a Bradesco rewards portal
- **Actual URL:** Links to an unknown third-party site not associated with Bradesco
- **Detection:** Mismatch discovered by **hovering over the link**, revealing the real target

---

## ✍️ 7. Spelling and Grammar Review

- **Language:** Portuguese
- **Tools can you use** [QuillBot](https://quillbot.com/spell-checker)
- **Errors Observed:** Minor inconsistencies in spacing and formatting, typical of phishing templates, though no obvious spelling mistakes were found.
- **Suspicion Trigger:** Unprofessional formatting and design quality

---

## ✅ 8. Summary of Phishing Traits

| Trait | Description |
|-------|-------------|
| 📧 **Spoofed Sender** | Fake Bradesco-looking email address |
| 🧾 **Header Discrepancies** | SPF, DKIM, DMARC all failed |
| 🔗 **Suspicious Link** | Redirects to non-Bradesco URL |
| ⏰ **Urgency** | Threatens point expiration “today” |
| 🔍 **Link Mismatch** | Hover reveals different destination |
| ✍️ **Unpolished Format** | Basic design inconsistencies raise red flags |

---

## 💡 Conclusion

This email is a **confirmed phishing attempt** that leverages brand impersonation, urgency, and deceptive links to manipulate users. It demonstrates how attackers use psychological pressure and visual mimicry to lure victims into fraud.

---

## 🧰 Tools Used

- `.eml` Viewer (Thunderbird, Outlook)
- Google Admin Toolbox Header Analyzer
- Base64/HTML Decoders
- Manual Link Inspection

---

## 📌 Disclaimer

This repository is for **educational and awareness purposes only**. Do not attempt to engage with or forward phishing content unless you're authorized to investigate cyber threats.

---





