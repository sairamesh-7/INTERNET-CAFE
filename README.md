# INTERNET-CAFE
📡 Internet Café Network Design – Case Study
A Complete Network Architecture, Configuration & Validation Project

Course: 21CSC302J – Computer Networks
Student: Pragada Sai Ramesh (RA2311028010045)
Institution: SRM Institute of Science and Technology
Year: November 2025

📘 Project Overview

This project focuses on designing a secure, scalable, and efficient network for an Internet Café with 30 client PCs, an ADSL internet connection, and internal services such as billing, web filtering, and PC monitoring.

The goal was to create a network layout that ensures:

✅ Smooth and stable internet access
✅ Secure browsing for users
✅ Efficient customer billing & PC usage tracking
✅ Proper IP addressing & network organization
✅ Easy future expansion

The design includes detailed topology creation, IP planning, device configuration, testing, and evaluation.

🏗️ Network Architecture
✅ Topology Used: Star Topology

All 30 PCs are connected through two switches to a central router, which connects to the ADSL modem.

📌 Key Components
Device	Purpose
Router (1)	Acts as gateway, DHCP server, NAT, firewall
Switches (2)	Connect internal PCs and servers
Servers (2)	Billing system, web filtering, backup services
Admin PC (1)	Network monitoring and management
Client PCs (30)	Internet café user systems
ADSL Modem	ISP-provided WAN access
🌐 IP Addressing Scheme

Private network: 192.168.1.0/24
Public/DMZ: 200.0.0.0/24

✅ Static IPs

Server0 (Billing/Web Filter): 192.168.1.10

Admin PC: 192.168.1.2

Router LAN: 192.168.1.1

Server1 (External/DMZ): 200.0.0.10

Router WAN: 200.0.0.1

✅ Dynamic IPs

Client PCs: 192.168.1.3 – 192.168.1.33 (via DHCP)

This structured addressing ensures seamless communication and zero IP conflicts.

⚙️ Configuration Summary
✅ Router Configuration

LAN: 192.168.1.1/24

WAN: 200.0.0.1/24

DHCP range: 192.168.1.3 – 192.168.1.33

NAT enabled for shared internet access

Default gateway for all internal devices: 192.168.1.1

✅ Switch Configuration

Unmanaged – plug-and-play

Switch0 connects router, servers, admin PC, Switch1

Switch1 connects all 30 PCs

✅ Server Configuration

Server0: Local services (billing, web filtering) on 192.168.1.10

Server1: External/DMZ operations on 200.0.0.10

✅ Client PCs

Set to obtain IP automatically via DHCP

Direct browser access to billing system: http://192.168.1.1

🧪 Testing & Validation
✅ Connectivity Tests

Ping router from PC1 and Admin PC → Successful

Inter-PC communication tested via ping → Successful

✅ Billing System Testing

A dynamic website was created using HTML, CSS, and JavaScript to:

Display PC status (Free / Occupied)

Add or logout customers

Auto-calculate billing amount

Maintain billing history

Accessible locally at:
👉 http://192.168.1.1

✅ DHCP Testing

All client PCs successfully received dynamic IPs

No IP conflicts detected

✅ Router Verification

Using commands:

show ip interface brief
show ip route


All interfaces and routing tables validated successfully.

✅ Results

Entire network performs smoothly with 30 simultaneous users.

Billing & monitoring system works in real time.

Web filtering ensures safe browsing.

Network structure is scalable for future growth.

Configuration remains stable after reboot.

📌 Project Conclusion

This project successfully demonstrates the complete design, implementation, and testing of a small-scale Internet Café network.
The final system:

✅ Ensures fast, stable connectivity
✅ Provides secure and filtered browsing
✅ Automates billing and PC monitoring
✅ Uses cost-effective and scalable design principles

The solution is practical, reliable, and well-suited for real-world café operations.

📚 References

GeeksforGeeks – DHCP Server Configuration

Cisco Packet Tracer Documentation

Kaur, G., & Shukla, V. – Internet Café Network Design (IJCSMC)

📄 Appendix – Common Terms
Abbreviation	Full Form
LAN	Local Area Network
WAN	Wide Area Network
DHCP	Dynamic Host Configuration Protocol
NAT	Network Address Translation
ISP	Internet Service Provider
OSI	Open Systems Interconnection
FTP	File Transfer Protocol
HTTP	Hypertext Transfer Protocol
