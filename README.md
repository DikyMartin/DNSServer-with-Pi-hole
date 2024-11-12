# Building DNS Server With Pi-hole

Pi-hole is a DNS server application focused on DNS sinkhole functions. This application features ad and website blocking, which helps enhance the security of private networks.

This DNS sinkhole software was first created by Jacob Salmela in 2014. The application is built at the Linux network level and is available for free. Pi-hole was released as open-source on GitHub, and over time, several contributors have joined to help develop this project.

Pi-hole allows you to block ads and specific websites within your network. The name Pi-hole comes from the fact that the application was originally designed for Raspberry Pi. However, you can now use it on virtual machines or any hardware running Ubuntu, Debian, Fedora, or CentOS. [MORE](https://idcloudhost.com/blog/apa-itu-pi-hole/)

## Preparation & Information

Here, I will be using a virtual machine, specifically VirtualBox, with [DEBIAN](https://www.debian.org/download) as the operating system.

I will only test the capabilities of Pi-hole adblocker, with a comparison of a website that already uses Pi-hole and has not used Pi-hole. And using the blacklist feature to block unwanted websites. For VirtualBox Debian I use 2 adapters, with adapter 1 as NAT and adapter 2 as Host-Only Adapter. For the IP, adapter 1 is set to DHCP and adapter 2 is set statically with IP 192.168.100.1 with a range of 10 - 50.

### Installation

