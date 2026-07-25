# 🔥 Task 2 - Basic Firewall Configuration using UFW

## 📌 Objective

The objective of this task is to configure a basic firewall using **UFW (Uncomplicated Firewall)** to control network traffic, secure a Linux system, and understand the importance of firewall rules in protecting a machine from unauthorized access.

---

## 🛠️ Tools Used

* Kali Linux / Ubuntu
* UFW (Uncomplicated Firewall)
* Linux Terminal

---

## 📖 What is UFW?

**UFW (Uncomplicated Firewall)** is a user-friendly command-line firewall utility that simplifies the management of **iptables**. It allows users to create and manage firewall rules without dealing with complex configurations.

---

## ❓ Why Firewall Configuration Matters?

Firewalls are the first line of defense for a system. They help to:

* Block unauthorized network access
* Allow only trusted connections
* Reduce the attack surface
* Protect services from unwanted traffic
* Improve overall system security

---

## 🔧 Installation & Setup

Update the package list:

```bash
sudo apt update
```

Install UFW:

```bash
sudo apt install ufw -y
```

Check the firewall status:

```bash
sudo ufw status
```

Enable the firewall:

```bash
sudo ufw enable
```

### Default Policies

* Deny all incoming connections
* Allow all outgoing connections

---

## 🔐 Firewall Rules

### Allow SSH (Port 22)

```bash
sudo ufw allow ssh
```

### Deny HTTP (Port 80)

```bash
sudo ufw deny http
```

### Allow HTTPS (Port 443)

```bash
sudo ufw allow https
```

---

## 📊 Verify Firewall Status

Display all active firewall rules:

```bash
sudo ufw status verbose
```

Expected Result:

* Firewall is active
* SSH traffic is allowed
* HTTP traffic is denied
* HTTPS traffic is allowed
* Default policies are applied successfully


---

## 📸 Screenshots

The following screenshots are included in the **screenshots** folder:

* UFW installation
* Firewall enabled successfully
* Firewall rule configuration
* UFW status verification

---


## ⚠️ Ethical Use

This task was completed on a personal virtual machine for educational purposes only. Firewall configurations should only be performed on systems that you own or have explicit permission to manage.

---

## 📚 Learning Outcomes

* Installed and configured UFW
* Applied firewall rules to allow and deny traffic
* Verified firewall configuration
* Learned the importance of firewall security
* Documented the complete configuration process
