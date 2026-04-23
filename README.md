# FUTURE_CS_01

Cyber Security Internship Portfolio – Future Interns

---

# 🔐 Task 1 – Vulnerability Assessment Report

---

## 🎯 Objective

This assessment aims to identify potential security weaknesses in a publicly accessible web application using safe, ethical, and non-intrusive testing methods.

The focus is on analyzing risks, understanding their potential impact, and recommending practical mitigation strategies.

---

## 🌐 Target Application

http://testfire.net/

---

## 📌 Scope

* Assessment limited to publicly accessible pages
* Strictly read-only (no exploitation performed)
* Passive and ethical testing methodology followed

---

## 🛠️ Tools & Technologies

* **Nmap** → Network scanning and service detection
* **OWASP ZAP** → Passive vulnerability identification
* **Browser DevTools** → Inspection of headers and cookies

---

# 🔎 Analysis & Findings

---

## 📡 1. Network Analysis (Nmap)

### 🔹 Commands Executed

* `nmap -sV testfire.net`
* `nmap -A testfire.net`

### 📸 Evidence

<img width="1043" height="557" alt="intern tsak 1 1" src="https://github.com/user-attachments/assets/6de1692d-2799-41f8-a93d-fefd86b3d582" />

<img width="1658" height="838" alt="intern task 1 2" src="https://github.com/user-attachments/assets/971d9bd2-985f-4f51-9e51-956814b1b7a3" />


### ⚠️ Key Findings

**Open HTTP Port (80)**

* Risk Level: Medium
* Data transmission occurs without encryption, increasing interception risk

**Server Information Exposure**

* Risk Level: Low
* Server details are disclosed, aiding potential attackers

---

## 🛡️ 2. Vulnerability Assessment (OWASP ZAP)

### 📸 Scan Results

<img width="1782" height="518" alt="zap3" src="https://github.com/user-attachments/assets/a8b23f86-4b95-4bb1-ac60-9a1196734f67" />  

<img width="673" height="422" alt="zap4" src="https://github.com/user-attachments/assets/749cf207-9c5a-4a54-a601-670ebc154ce6" />  

<img width="1917" height="552" alt="zap5" src="https://github.com/user-attachments/assets/a310fef7-3645-4cce-bebf-18ea5fae191e" />  

### ⚠️ Identified Issues

**Absence of Anti-CSRF Tokens**

* Risk Level: Medium
* May allow unauthorized actions on behalf of users

**Missing Content Security Policy (CSP)**

* Risk Level: Medium
* Increases exposure to Cross-Site Scripting (XSS) attacks

**Missing Anti-Clickjacking Protection**

* Risk Level: Low
* Allows potential UI redressing attacks

**Cookies Missing SameSite Attribute**

* Risk Level: Medium
* Increases susceptibility to CSRF attacks

---

## 🧪 3. Security Configuration Review (Browser DevTools)

### 📸 Evidence

<img width="1912" height="757" alt="devtool2" src="https://github.com/user-attachments/assets/36ec1c42-27db-4702-aeb8-cb73dfa75521" />  

### ⚠️ Observations

**Missing Security Headers**

* Risk Level: Medium
* Essential headers such as CSP and X-Frame-Options are not implemented

**Weak Cookie Security Configuration**

* Risk Level: Medium
* Missing Secure, HttpOnly, and SameSite attributes

---

# 📊 Risk Overview

| Vulnerability                   | Risk Level |
| ------------------------------- | ---------- |
| Open HTTP Port                  | Medium     |
| Server Information Disclosure   | Low        |
| Missing Content Security Policy | Medium     |
| Lack of CSRF Protection         | Medium     |
| Clickjacking Risk               | Low        |
| Insecure Cookie Configuration   | Medium     |

---

# 🧾 Conclusion

The assessment revealed multiple security misconfigurations primarily related to missing protections and weak configurations.

Although no active exploitation was performed, these vulnerabilities could be leveraged by attackers if left unaddressed. Strengthening these areas will significantly enhance the application’s security posture.

---

# ✅ Recommendations

* Enforce HTTPS across all endpoints
* Implement essential security headers (CSP, X-Frame-Options, etc.)
* Configure cookies securely with appropriate flags
* Limit exposure of server-related information
* Conduct periodic security assessments

---

# 📘 Learning Outcomes

* Gained practical experience in vulnerability assessment
* Improved understanding of common web security risks
* Hands-on exposure to industry-standard security tools

---

## 📄 Report Access

The complete vulnerability assessment report is available here:
https://github.com/Jebin7777/FUTURE_CS_01/blob/main/REPORT.pdf

---

## 👤 Author

**Jebin A**
Cyber Security Intern – Future Interns
