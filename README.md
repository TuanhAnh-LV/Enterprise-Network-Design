Secure Enterprise Network Architecture (HQ & Branch)

📌 Project Overview

This project simulates a comprehensive enterprise network for a company with a Headquarter (HQ) and a Branch office. The primary focus is on high availability, scalability, and robust security hardening across Layer 2 and Layer 3.

🌐 Network Topology

Topology designed and simulated using Cisco Packet Tracer.

🚀 Key Technical Features

1. Connectivity & Routing
   
Site-to-Site IPsec VPN: Established a secure tunnel for encrypted communication between HQ and Branch.

Dynamic Routing: 

  eBGP: Configured for external ISP connectivity.
  
  OSPF Multi-area: Implemented for efficient internal routing and reduced SPF overhead.

NAT: Extended NAT configuration to allow internal VLANs to access the Internet.

2. High Availability & Switching (L2/L3)
   
Redundancy: Used HSRP (Hot Standby Router Protocol) for gateway redundancy.

Loop Prevention & Load Balancing: Configured PVST+ to distribute VLAN traffic across DSW1 and DSW2 (Root Bridge optimization).

Link Aggregation: LACP EtherChannel between distribution switches to increase bandwidth and reliability.

VTP: Managed VLAN database consistency across the campus network.

3. Security Hardening (The Core)
   
L2 Security:

  DHCP Snooping & Dynamic ARP Inspection (DAI): Mitigating Man-in-the-Middle (MitM) and ARP poisoning attacks.
  
  Port Security: Restricting access based on MAC addresses.

Traffic Control: Used Extended ACLs to enforce strict policies:

  Guest VLAN: Internet access only, isolated from internal resources.
  
  HR VLAN: Only access to internal HR resources, no Internet and cross-department access.

AAA/Wireless: Integrated WLC with RADIUS for centralized authentication.

🛠 Tools & Technologies

Simulation: Cisco Packet Tracer.

Protocols: IPsec, BGP, OSPF, HSRP, LACP, PVST+, IEEE 802.1Q.

Security: ACL, AAA, Port Security, DHCP Snooping, DAI.
