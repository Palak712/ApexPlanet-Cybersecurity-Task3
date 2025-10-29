Web Application Security is performed hands-on testing of web vulnerabilities such as SQL Injection, XSS, CSRF, and File Inclusion using DVWA hosted on Kali Linux. Includes attack demonstrations, mitigation techniques, Burp Suite intercepts, security headers, and lab documentation. 

## 🧠 Overview
This project focuses on understanding, exploiting, and securing *web applications* against common vulnerabilities using *DVWA (Damn Vulnerable Web App)* hosted on *Kali Linux*.  
The main goal was to simulate real-world attack vectors (in a safe lab) and apply security controls to mitigate them.

---

## 🧩 Learning Objectives
- Understand how vulnerabilities like *SQL Injection, XSS, CSRF, and File Inclusion* work.
- Perform attacks safely in a controlled lab environment.
- Analyze and report findings with evidence and mitigations.
- Strengthen understanding of *web security principles* and *secure coding*.

---

## 🧰 Tools & Technologies
| Category | Tools Used |
|-----------|-------------|
| OS / Platform | Kali Linux, DVWA (PHP/MySQL), Apache Server |
| Scanning & Exploitation | Burp Suite, SQLMap, OWASP ZAP |
| Utilities | Wireshark, Curl, Firefox, Netcat |
| Scripting | Bash / HTML / PHP (for exploit simulation) |

---

## 🧪 Lab Setup
| Machine | Role | IP | Description |
|----------|------|---|--------------|
| Kali Linux | Attacker | 192.168.56.101 | Used for exploiting vulnerabilities |
| DVWA (on Target VM) | Victim | 192.168.56.102 | Vulnerable web app for testing |
| Network | Host-Only | 192.168.56.0/24 | Isolated and safe for testing |

---

## 🔍 Tasks Performed

### 1. SQL Injection (SQLi)
- Manual Injection: ' OR '1'='1' --  
- Automated using *SQLMap*:
  ```bash
  sqlmap -u "http://192.168.56.102/dvwa/vulnerabilities/sqli/?id=1&Submit=Submit" --cookie="PHPSESSID=xxx; security=low" --batch --dbs
