# Phishing Investigation – Credential Harvesting Analysis

## 📌 Overview
This project documents a hands-on phishing investigation lab completed on TryHackMe. The objective was to analyze a phishing email, investigate malicious infrastructure, and identify how attackers collect user credentials.

---

## 🎯 Objectives
- Analyze a phishing email and identify indicators of compromise
- Investigate malicious URLs and redirections
- Identify phishing infrastructure and exposed directories
- Analyze phishing kit contents
- Detect how credentials are captured and exfiltrated

---

## 🔍 Investigation Process

### 1. Email Analysis
- Identified suspicious sender domain
- Noted external sender warning
- Detected phishing indicators (urgent tone, attachment)

---

### 2. Attachment Analysis
- Opened HTML attachment in a controlled environment
- Observed redirection to a fake Microsoft login page
- Detected insecure connection (no HTTPS)

---

### 3. Phishing Site Investigation
- Analyzed phishing URL:
  kennaroads.buzz
- Identified fake Microsoft login page impersonation

---

### 4. Directory Enumeration
- Discovered exposed directory:
  /data
- Found phishing kit files:
  - Update365.zip
  - Update365/

---

### 5. Phishing Kit Analysis
- Downloaded and extracted phishing kit
- Explored internal structure:
  - office365/
  - PHP scripts
  - Log files

---

### 6. Hash Analysis
Generated SHA256 hash of phishing kit:

---

### 7. Credential Harvesting Analysis
- Located backend PHP script handling credentials
- Extracted attacker email used for exfiltration:

- Observed captured data:
  - Email
  - Password
  - IP Address
  - User Agent
  - Country

---

### 8. Log Analysis
- Identified multiple credential submissions
- Confirmed attacker data collection activity

---

## 🚨 Key Findings
- Fake Microsoft login phishing page detected
- Credentials captured via POST request
- Data sent to attacker-controlled email
- Poor server security exposed sensitive directories and files

---

## 🛠 Tools Used
- TryHackMe AttackBox
- Linux Terminal
- sha256sum
- Web Browser (Firefox)
- CyberChef (for decoding)

---

## 🧠 Skills Demonstrated
- Phishing Detection
- Threat Analysis
- Web Enumeration
- Malware Analysis (Basic)
- Incident Investigation

---

## 📈 Key Takeaway
This lab demonstrates how attackers exploit misconfigured servers and use phishing kits to harvest credentials. It highlights the importance of secure configurations, user awareness, and proactive threat detection.

---

## 🚀 Author
Oluwatoyin Oyedijo  
Aspiring SOC Analyst | Cybersecurity Enthusiast
