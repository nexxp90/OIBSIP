🔥 Task 2 - Basic Firewall Configuration using UFW
📌 Objective

The objective of this task is to configure a basic firewall using UFW (Uncomplicated Firewall) to manage network traffic and improve the security of a Linux system.

🛠️ Tools Used
Kali Linux / Ubuntu
UFW (Uncomplicated Firewall)
Linux Terminal
📖 What is UFW?

UFW (Uncomplicated Firewall) is a command-line firewall tool designed to simplify the management of iptables. It allows users to easily allow or block incoming and outgoing network traffic.

❓ Why Firewall Configuration Matters

A firewall helps protect a system by:

Blocking unauthorized network access
Allowing only trusted connections
Reducing the attack surface
Improving overall system security

🔧 Firewall Installation
UFW was installed using the following command:

sudo apt install ufw -y
Enabling the Firewall
The firewall was enabled to start enforcing rules:

sudo ufw enable
Default policies applied:
Deny all incoming connections

Allow all outgoing connections

🔐 Configuring Firewall Rules
Allow SSH (Port 22)
To maintain remote access, SSH traffic was allowed:

sudo ufw allow ssh
Deny HTTP (Port 80)
HTTP traffic was blocked to demonstrate firewall filtering:

sudo ufw deny http
📊 Firewall Status Verification
Firewall status and rules were verified using:

sudo ufw status verbose
This confirmed:
Firewall is active

SSH allowed

HTTP denied

Default policies enforced

📷 Screenshots
All relevant screenshots showing firewall installation, rule configuration, and status verification are included in the screenshots directory.


⚠️ Ethical Use

This firewall configuration was performed on a personal virtual machine for learning purposes. Do not modify firewall rules on production systems without proper authorization.

📚 Learning Outcome
Installed and configured UFW
Allowed and blocked network ports
Verified firewall status
Understood the importance of firewall protection
Documented the configuration process
