# 🔍 Task 1 - Basic Network Scanning with Nmap

## 📌 Objective

The goal of this task is to perform basic network reconnaissance using **Nmap** to discover open ports, identify running services, detect the target operating system, and analyze the security impact of the discovered services.

---

## 🛠️ Tools Used

* Kali Linux (VirtualBox)
* Nmap
  

---

## 📖 What is Nmap?

**Nmap (Network Mapper)** is a powerful open-source tool used for network discovery and security auditing. It helps identify active hosts, open ports, running services, and operating systems on a network.

---

## ❓ Why Network Scanning Matters

Network scanning helps administrators and security professionals:

* Discover open ports and running services
* Identify unnecessary or exposed services
* Detect potential security risks
* Improve the overall security posture of a system


---

## 🚀 Scans Performed

### 1. Basic Scan

```bash
nmap 127.0.0.1
```

Discovers active hosts and open TCP ports.

---

### 2. Service Version Detection

```bash
nmap -sV 127.0.0.1
```

Identifies the version of services running on open ports.

---

### 3. Operating System Detection

```bash
sudo nmap -O 127.0.0.1
```

Attempts to detect the target operating system.

---

## 📊 Open Ports Analysis

| Port | Service | Description         | Security Risk                                                |
| ---- | ------- | ------------------- | ------------------------------------------------------------ |
| 22   | SSH     | Secure remote login | Weak passwords may allow unauthorized access                 |
| 80   | HTTP    | Web server          | Outdated web applications may contain vulnerabilities        |
| 443  | HTTPS   | Secure web service  | Misconfiguration or expired certificates can weaken security |

> *The ports listed above are sample results. Your actual scan results may differ.*

---

## 📂 Project Structure

```text
Task-1-Basic Network Scanning with Nmap/
│
├── README.md
├── nmap_scan_results.txt
└── screenshots/
    ├── basic_scan.png
    ├── service_scan.png
    └── os_detection.png
```

---

## 📸 Screenshots

Include screenshots of:

* Basic scan output
* Service version scan
* OS detection scan

Store all screenshots inside the **screenshots/** folder.

---

## 📄 Output File

Create a file named:

```text
nmap_scan_results.txt
```

This file should contain:

* Target IP
* Commands executed
* Open ports
* Running services
* OS detection results
* Security observations

---

## ⚠️ Ethical Use

This task was performed only in a controlled lab environment using a local virtual machine. Never scan systems without proper authorization or permission.

---

## 📚 Learning Outcome

* Installed and configured Nmap
* Performed network reconnaissance
* Identified open ports and running services
* Detected the operating system
* Analyzed basic security risks
* Documented findings in a professional format
