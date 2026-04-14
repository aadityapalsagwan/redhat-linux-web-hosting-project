# 🚀 Website Hosting on Red Hat Linux 10 using Apache | VMware Project

![Project Banner](screenshots/Screenshot%202026-04-14%20153614.png)

---

## 📌 Project Overview

This project demonstrates deployment of a static website on **Red Hat Enterprise Linux 10** using **Apache HTTP Server (httpd)** inside VMware.

The goal of this project was to simulate a real-world Linux web hosting environment by configuring Apache, managing firewall and SELinux policies, and troubleshooting VMware network conflicts.

---

## 🎯 Objectives

✅ Install Red Hat Linux 10 on VMware  
✅ Configure Apache Web Server  
✅ Host static website successfully  
✅ Enable HTTP access using firewall rules  
✅ Troubleshoot SELinux restrictions  
✅ Resolve VMware network adapter conflicts  
✅ Access hosted website from laptop/mobile browser  

---

## 🛠 Technologies Used

- Red Hat Enterprise Linux 10  
- VMware Workstation  
- Apache HTTP Server (httpd)  
- systemctl  
- journalctl  
- firewalld  
- SELinux  
- Linux Networking Commands  

---

## ⚙️ Commands Used

```bash
dnf install httpd -y
systemctl start httpd
systemctl enable httpd
systemctl status httpd

firewall-cmd --permanent --add-service=http
firewall-cmd --reload
firewall-cmd --list-all

getenforce
setenforce 0
restorecon -Rv /var/www/html

journalctl -u httpd
journalctl -u httpd -n 20

ip a
ss -tulnp | grep :80
curl http://192.168.16.144

🌐 Website Output
Hosted Website Successfully Running:

📷 Project Screenshots
1️⃣ Apache Service Running Status

2️⃣ Firewall Configuration

3️⃣ Website Browser Output

4️⃣ Website Source Code

🔍 Issues Resolved
✅ Apache Startup Issue

Resolved Apache service startup and port listening issue.

✅ SELinux Blocking HTTP Access

Detected and fixed SELinux restrictions causing external access denial.

✅ VMware Network Adapter Conflict

Resolved VMnet adapter conflict preventing laptop browser access.

📁 Project Folder Structure

redhat-linux-web-hosting-project/
│
├── README.md
├── index.html
├── commands-used.txt
├── screenshots/
│   ├── Screenshot 2026-04-14 155734.png
│   ├── Screenshot 2026-04-14 155854.png
│   ├── Screenshot 2026-04-14 153614.png
│   └── Screenshot 2026-04-14 155007.png
│
└── configs/
    └── httpd.conf


💡 Key Learnings
Apache Web Server Deployment
Linux Service Management using systemctl
SELinux Troubleshooting
Firewall Rule Configuration
VMware Networking Debugging
Real-world Linux Hosting Environment Setup


👨‍💻 Author
Aaditya Pal

Linux & Cloud Enthusiast
Red Hat Linux | AWS | Apache | VMware

GitHub Repository
https://github.com/aadityapalsagwan/redhat-linux-web-hosting-project