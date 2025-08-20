# Building a Pi-hole DNS Server for Network Security

## 📌 Overview
This project demonstrates how to set up a **DNS server with Pi-hole** on Debian 11 using VirtualBox.  
The purpose of this setup is to **increase network security** and **improve privacy** by blocking ads, malware, trackers, and unwanted websites at the DNS level.  

Unlike browser-based ad blockers, Pi-hole works on the **entire network**, so every device connected to your network will benefit from DNS filtering automatically.  

---

## 🚀 Features
- **Ad & Tracker Blocking** → Block advertisements and tracking domains across all devices.  
- **DNS Sinkhole Technology** → Prevent connections to malicious or unwanted websites.  
- **Flexible Deployment** → Works on Raspberry Pi, Debian/Ubuntu servers, Fedora, or CentOS.  
- **Low Resource Usage** → Can run on small devices or virtual machines with minimal specs.  
- **Web Admin Dashboard** → Manage blacklists, whitelists, and monitor DNS queries in real time.  

---

## 🛠️ Tech Stack
- **Operating System**: Debian 11 (installed via VirtualBox)  
- **Core Service**: Pi-hole  
- **Virtualization**: Oracle VirtualBox  
- **Networking**:
  - Adapter 1: **NAT** (for internet access, DHCP enabled)  
  - Adapter 2: **Host-Only Adapter** (for internal network, static IP `192.168.100.1`)  

---

## 📖 Installation Guide

### 1. Update and clean system
```bash
sudo apt update
sudo apt upgrade -y
sudo apt clean

## ⚙️ Configuration Notes
- Select `enp0s8` as the network adapter (Host-Only, static IP).
- Recommended DNS: `quad9 (filtered, DNSSEC)`.
- Static IP configuration:
  - `192.168.100.1` with range `10 - 50`.

## 🌐 Accessing the Admin Panel
After installation, open a browser and go to:

## 🎯 Use Cases
- Students learning networking & Linux server administration.
- Small businesses seeking affordable network ad-blocking.
- Home users who want family-wide privacy protection.
- Educators teaching DNS and network security.

## 🔮 Future Improvements
- Integrate Pi-hole with Unbound for recursive DNS.
- Enable DNS-over-HTTPS (DoH) for encrypted DNS queries.
- Deploy on Raspberry Pi for 24/7 filtering.
- Automate deployment with Ansible or Docker.

## 📎 References
- [Pi-hole Official Website](https://pi-hole.net/)
- [Pi-hole GitHub Repository](https://github.com/pi-hole/pi-hole)
- [Debian Documentation](https://www.debian.org/doc/)

## 👨‍💻 Author
Created by **Diky Martin**  
💡 Contributions and feedback are welcome!
