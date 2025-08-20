# 🛡️ Pi-hole DNS Server for Network Security

![GitHub license](https://img.shields.io/github/license/DikyMartin/pi-hole-dns-server)
![GitHub last commit](https://img.shields.io/github/last-commit/DikyMartin/pi-hole-dns-server)
![GitHub stars](https://img.shields.io/github/stars/DikyMartin/pi-hole-dns-server)
![GitHub forks](https://img.shields.io/github/forks/DikyMartin/pi-hole-dns-server)

---

## 📑 Table of Contents
- [Overview](#overview)
- [Setup & Features](#setup--features)
- [Tech Stack & Networking](#tech-stack--networking)
- [Installation](#installation)
- [Topology](#topology)
- [Demo](#demo)
- [Use Cases](#use-cases)
- [Future Improvements](#future-improvements)
- [Useful Links](#useful-links)
- [Contributing](#contributing)
- [License](#license)

---

## 📌 Overview
This project demonstrates how to set up a **DNS server with Pi-hole** on Debian 11 using VirtualBox.  
The purpose of this setup is to **increase network security** and **improve privacy** by blocking ads, malware, trackers, and unwanted websites at the DNS level.  

Unlike browser-based ad blockers, Pi-hole works on the **entire network**, so every device connected will benefit from DNS filtering automatically.  
<img width="800" height="600" alt="dashboard pihole" src="https://github.com/user-attachments/assets/db42acab-5f80-4b3b-9ac8-5dfda76c25af" />

---

## ⚙️ Setup & Features
- **Ad & Tracker Blocking** → Block ads and tracking domains across all devices  
- **DNS Sinkhole Technology** → Prevent connections to malicious or unwanted websites  
- **Flexible Deployment** → Works on Raspberry Pi, Debian/Ubuntu servers, Fedora, or CentOS  
- **Low Resource Usage** → Runs on small devices or virtual machines with minimal specs  
- **Web Admin Dashboard** → Manage blacklists/whitelists and monitor DNS queries in real time  

### 🔧 Tech Stack & Networking
- **Operating System**: Debian 11 (installed via VirtualBox)  
- **Core Service**: Pi-hole  
- **Virtualization**: Oracle VirtualBox  
- **Networking Setup**:
  - Adapter 1: **NAT** → Internet access (DHCP enabled)  
  - Adapter 2: **Host-Only Adapter** → Internal network (static IP: `192.168.100.1`)  

---

## 🚀 Installation

### 1. Update and clean system
> sudo apt update

> sudo apt upgrade -y

> sudo apt clean

### 2. Install Pi-hole
> curl -sSL https://install.pi-hole.net | bash

If installation fails, use:

> curl -sSL https://install.pi-hole.net | sudo PIHOLE_SKIP_OS_CHECK=true bash

### 3. Set Admin Password
> pihole -a -p

---

## 🗺️ Topology

This setup uses **Debian 11 VM on VirtualBox** with two adapters:
- **Adapter 1 (NAT):** Internet access (via router 192.168.1.1)
- **Adapter 2 (Host-Only):** Internal network 192.168.100.0/24  
  → Pi-hole DNS server: `192.168.100.1`
<img width="837" height="435" alt="pihole_topology" src="https://github.com/user-attachments/assets/db3535a7-76e2-4199-98b7-fcb6aa0cec4d" />

---

## 🎯 Use Cases

- Students learning networking & Linux server administration.
- Small businesses seeking affordable network ad-blocking.
- Home users who want family-wide privacy protection.
- Educators teaching DNS and network security.

---

## 🔮 Future Improvements

- Integrate Pi-hole with Unbound for recursive DNS.
- Enable DNS-over-HTTPS (DoH) for encrypted DNS queries.
- Deploy on Raspberry Pi for 24/7 filtering.
- Automate deployment with Ansible or Docker.

---

## 🔗 Useful Links

- 🌐 [Pi-hole Official Website](https://pi-hole.net/)  
- 💻 [Pi-hole GitHub Repository](https://github.com/pi-hole/pi-hole)  
- 📖 [Debian Official Documentation](https://www.debian.org/doc/)  
- 🖥️ [Oracle VirtualBox Download](https://www.virtualbox.org/)  
- 📡 [Unbound DNS Resolver](https://www.nlnetlabs.nl/projects/unbound/about/)  
- 🔒 [DNS-over-HTTPS (DoH) RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484)  
- 🐧 [Linux Command Cheat Sheet](https://linuxcommand.org/lc3_learning_the_shell.php)  

---

![GitHub license](https://img.shields.io/github/license/DikyMartin/pi-hole-dns-server)
![GitHub last commit](https://img.shields.io/github/last-commit/DikyMartin/pi-hole-dns-server)
![GitHub stars](https://img.shields.io/github/stars/DikyMartin/pi-hole-dns-server)
![GitHub forks](https://img.shields.io/github/forks/DikyMartin/pi-hole-dns-server)
