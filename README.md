# Building DNS Server With Pi-hole

Pi-hole is a DNS server application focused on DNS sinkhole functions. This application features ad and website blocking, which helps enhance the security of private networks.

This DNS sinkhole software was first created by Jacob Salmela in 2014. The application is built at the Linux network level and is available for free. Pi-hole was released as open-source on GitHub, and over time, several contributors have joined to help develop this project.

Pi-hole allows you to block ads and specific websites within your network. The name Pi-hole comes from the fact that the application was originally designed for Raspberry Pi. However, you can now use it on virtual machines or any hardware running Ubuntu, Debian, Fedora, or CentOS. [MORE](https://idcloudhost.com/blog/apa-itu-pi-hole/)

## Preparation & Information

Here, I will be using a virtual machine, specifically VirtualBox, with [DEBIAN](https://www.debian.org/download) as the operating system.

I will only test the capabilities of Pi-hole adblocker, with a comparison of a website that already uses Pi-hole and has not used Pi-hole. And using the blacklist feature to block unwanted websites. For VirtualBox Debian I use 2 adapters, with adapter 1 as NAT and adapter 2 as Host-Only Adapter. For the IP, adapter 1 is set to DHCP and adapter 2 is set statically with IP 192.168.100.1 with a range of 10 - 50.

### Installation

#### Pi-hole installation
- >apt update
  
**Comment or delete the repository if there is a repository that fails to update**
- >apt upgrade -y
- >apt clean
- >curl -sSL https://install.pi-hole.net | bash

**if it fails to down use this**

>curl -sSL https://install.pi-hole.net | sudo
PIHOLE_SKIP_OS_CHECK=true bash

**Change password**

>pihole -a -p

## During installation

Just keep pressing yes
if there is a choice of enp0s3 or enp0s8
remember the adapter settings that are NAT and host-only adapter
ip enp0s8 must be static with a dhcp server
select enp0s8

**For DNS options select**
>quad9 (filtered, DNSSEC)

**Then into the browser**
>type 192.168.100.1/admin

(adjust the IP statistics)
select a domain if you want to block a website

Next, go to Windows, select the network connection feature
host-only adapter option that has been selected in Vbox

Next to IPV4 and write the dns according to the static ip enp0s8
which is 
>192.168.100.1

