# 🛡️ Building a Pi-hole DNS Server for Network Security

## 📌 Overview
This project demonstrates how to set up a **DNS server with Pi-hole** on Debian 11 using VirtualBox.  
The purpose of this setup is to **increase network security** and **improve privacy** by blocking ads, malware, trackers, and unwanted websites at the DNS level.  

Unlike browser-based ad blockers, Pi-hole works on the **entire network**, so every device connected will benefit from DNS filtering automatically.  

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
bash
> sudo apt update
> sudo apt upgrade -y
> sudo apt clean
