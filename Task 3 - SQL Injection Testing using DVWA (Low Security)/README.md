# 💉 Task 3 - SQL Injection Testing using DVWA (Low Security)

## 📌 Overview

This project demonstrates **SQL Injection** in **Damn Vulnerable Web Application (DVWA)** with the security level set to **Low**. The purpose of this task is to understand how improper input validation can lead to database vulnerabilities and why secure coding practices are important.

---

## 📋 Prerequisites

* **Operating System:** Windows 10/11
* **Software:** XAMPP (Apache + MySQL + PHP)
* **Browser:** Chrome / Firefox / Edge
* **Internet Connection:** Required to download DVWA

---

# 🚀 Installation & Setup

## Step 1: Install XAMPP

Download XAMPP from:

https://www.apachefriends.org/download.html

* Install XAMPP using the default settings.
* Open the **XAMPP Control Panel** after installation.

---

## Step 2: Start Required Services

From the XAMPP Control Panel:

* Start **Apache**
* Start **MySQL**

Both services should display a **green** status indicating they are running successfully.

---

## Step 3: Install DVWA

```text
# Download DVWA manually:
# 1. Go to: https://github.com/digininja/DVWA/archive/master.zip
# 2. Extract to: C:\xampp\htdocs\dvwa
```

---

## Step 4: Configure DVWA

Navigate to:

```text
C:\xampp\htdocs\dvwa\config
```

Copy:

```text
config.inc.php.dist
```

Rename it to:

```text
config.inc.php
```

Update the database configuration:

```php
$_DVWA['db_user'] = 'root';
$_DVWA['db_password'] = '';
$_DVWA['db_server'] = '127.0.0.1';
$_DVWA['db_database'] = 'dvwa';
```

---

## Step 5: Access DVWA

Open your browser and visit:

```text
http://localhost/dvwa/
```

Click **Create / Reset Database** and log in using:

* **Username:** admin
* **Password:** password

---

## Step 6: Set Security Level

Navigate to **DVWA Security** from the sidebar.

Select **Low** from the security level dropdown and click **Submit**.

---

# 🧪 SQL Injection Testing

### Test 1 – SQL Error Detection

**Payload**

```text
'
```

**Observation**

The application returned a SQL error, indicating that user input is directly included in the database query without proper validation.

---

### Test 2 – Retrieving Records

**Payload**

```text
' OR '1'='1
```

**Observation**

The query returned multiple records from the database, demonstrating how SQL Injection can manipulate the application's SQL query.

---

### Test 3 – Database Information Disclosure

**Payload**

```text
' UNION SELECT NULL, version() #
```

**Observation**

The application displayed the MySQL server version, showing how attackers may gather information about the database environment.

---

### Test 4 – Data Extraction

**Payload**

```text
' UNION SELECT user, password FROM users #
```

**Observation**

The query displayed usernames and password hashes stored in the database, highlighting the impact of insecure SQL queries.

---

# 📷 Screenshots

Include screenshots for:

* DVWA Installation
* Login Page
* Security Level (Low)
* SQL Injection Module
* SQL Error Output
* Record Retrieval
* Database Version
* Data Extraction Result

---

# 🔍 Security Analysis

### Root Cause

* Improper input validation
* Dynamic SQL queries without parameterized statements

### Risk Level

**Severity:** High

Potential Risks:

* Information disclosure
* Database enumeration
* Exposure of sensitive data
* Unauthorized access to stored information

---

# 🛡️ Recommended Mitigations

* Use Prepared Statements (Parameterized Queries)
* Validate and sanitize all user inputs
* Apply the Principle of Least Privilege
* Deploy a Web Application Firewall (WAF)
* Perform regular security testing and code reviews

---

# ⚠️ Ethical Note

This demonstration was performed only on a locally hosted **DVWA** environment created for educational and security training purposes. Do not perform these tests on systems without explicit authorization.

---

# 📚 References

* OWASP SQL Injection Prevention Cheat Sheet
* DVWA Official Documentation
* MySQL Security Best Practices

---

## 🎯 Learning Outcome

* Installed and configured DVWA
* Performed SQL Injection testing in a controlled environment
* Identified how insecure SQL queries expose database information
* Understood the importance of input validation and parameterized queries
* Learned common mitigation techniques against SQL Injection
