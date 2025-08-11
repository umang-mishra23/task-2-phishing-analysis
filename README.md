# Task 2 — Phishing Email Analysis

## 📌 Objective
Analyze a phishing email sample to identify suspicious characteristics, including spoofing, malicious links, urgent tone, and technical header discrepancies.

---

## 📂 Files in This Repo
- `phishing_email.txt` → Raw phishing email text
- `headers_analysis.txt` → Results from header analyzer
- `screenshots/` → Visual proof of phishing email and header analysis

---

## 🔍 Phishing Indicators Found

| Indicator | Evidence | Why It’s Suspicious | Risk |
|-----------|----------|---------------------|------|
| **Spoofed Sender** | `support@paypa1.com` | Domain misspelled (`1` instead of `l`) | Users may think it’s legitimate |
| **Mismatched URL** | Link text: PayPal → Real URL: `secure-paypal-login.com` | Leads to phishing site | Credential theft |
| **Urgent Tone** | “Verify within 24 hours or account closed” | Pressures quick action | Social engineering |
| **Attachment** | `Account_Verification_Form.zip` | Could contain malware | System compromise |
| **Poor Grammar** | “Thank you for your prompt attention” (odd phrasing) | Not standard corporate language | Trust manipulation |

---

## 🛠 Header Analysis
Key findings from `headers_analysis.txt`:
- **SPF: FAIL** — Sender not authorized for PayPal domain.
- **DKIM: FAIL** — No valid DKIM signature.
- **DMARC: FAIL** — Spoofed sender bypassed checks.
- **Source IP** from Russia — does not match PayPal’s US-based servers.

---

## ⚠ Risk Assessment
- **Credential Theft**: Fake login page steals usernames & passwords.
- **Malware Infection**: ZIP file could contain trojan/virus.
- **Social Engineering**: Creates urgency to bypass rational thinking.

---

## 🔒 Recommended Actions
- Do not click links or open attachments.
- Report to PayPal via their phishing email address: `phishing@paypal.com`.
- Block sender’s domain and IP.
- Educate users about checking email headers.

---

## 📸 Screenshots

<img width="1536" height="1024" alt="ChatGPT Image Aug 11, 2025, 04_56_15 PM" src="https://github.com/user-attachments/assets/d6387947-8564-44e8-8484-f5e05eec453c" />


---

## 📚 References
- [Phishing.org Examples](https://www.phishing.org/phishing-examples)
- [MXToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)
- [Google Email Header Tool](https://toolbox.googleapps.com/apps/messageheader/)
