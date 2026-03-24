<div align="center">
   <h1> Secure Enterprise Network Architecture (HQ & Branch) </h1>
</div>

## 📌 Project Overview

This project simulates a comprehensive enterprise network for a company with a Headquarter (HQ) and a Branch office. The primary focus is on high availability, scalability, and robust security hardening across Layer 2 and Layer 3.

## 🌐 Network Topology

Topology designed and simulated using Cisco Packet Tracer.
<img width="1997" height="1598" alt="topo" src="https://github.com/user-attachments/assets/8079c911-f775-42fb-ace8-100085549995" />

## 🚀 Key Technical Features

#### 1. Connectivity & Routing
   
* **Site-to-Site IPsec VPN:** Established a secure tunnel for encrypted communication between HQ and Branch.
* **eBGP:** Configured for external ISP connectivity and public routing.
* **OSPF Multi-area:** Implemented for efficient internal routing and reduced SPF calculation overhead.
* **Extended NAT:** Configured to allow specific internal VLANs to access the Internet securely.

#### 2. High Availability & Switching (L2/L3)
   
* **Redundancy:** Used HSRP (Hot Standby Router Protocol) for gateway redundancy.

* **Loop Prevention & Load Balancing:** Configured PVST+ to distribute VLAN traffic across DSW1 and DSW2 (Root Bridge optimization).

* **Link Aggregation:** LACP EtherChannel between distribution switches to increase bandwidth and ensure link-level reliability.

* **VTP (VLAN Trunking Protocol):** Maintained consistent VLAN database management across the campus network.

#### 3. Security Hardening 
   
* **DHCP Snooping & Dynamic ARP Inspection (DAI):** Mitigated Man-in-the-Middle (MitM) and ARP poisoning attacks at the access layer.
* **Port Security:** Restricted unauthorized network access based on strict MAC address policies.

* **Traffic Control (Extended ACLs):** Enforced strict departmental isolation (e.g., Guest VLAN limited to Internet only; HR VLAN restricted to internal resources with no Internet access).

* **AAA & Wireless Security:** Integrated a Wireless LAN Controller (WLC) with a RADIUS server for centralized 802.1X authentication.

## 🛠 Tools & Technologies

| Category | Technologies & Protocols |
| :--- | :--- |
| **Simulation Tool** | Cisco Packet Tracer |
| **Routing & Switching** | BGP, OSPF, HSRP, LACP, PVST+, IEEE 802.1Q, VTP |
| **Network Security** | IPsec VPN, Extended ACLs, AAA (RADIUS), Port Security, DHCP Snooping, Dynamic ARP Inspection (DAI) |

