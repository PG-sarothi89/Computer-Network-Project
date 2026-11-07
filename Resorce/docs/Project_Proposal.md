Department of Information and Communication Technology

Faculty of Science and Technology

Bangladesh University of Professionals

Course Name: Computer Network Laboratory

Course Code: ICE 2208

Project Proposal

Secure Multi-Branch Enterprise Network WAN Simulation for GlobalTech Industries Ltd.

Date of Submission: 30/9/2026

Supervised by:

Sharmeen Jahan Seema

Lecturer

Department of ICT, FST

Bangladesh University of Professionals

Submitted by:

Partho Sarothi Ghosh

ID: 24549010089

Section: B

BICE 2025

Aritry Talukdar

ID: 24549010069

Section: B

BICE 2025

1. Project Overview

This project simulates a secure, redundant multi-branch enterprise WAN for a fictional company, GlobalTech Industries Ltd., in Cisco Packet Tracer. The network connects a Dhaka headquarters (HQ) with twenty regional branches across Bangladesh (Chattogram, Rajshahi, Khulna, Sylhet, Barishal, Rangpur, Mymensingh, Comilla, Gazipur, Narayanganj, Bogra, Coxs Bazar, Jessore, Dinajpur, Tangail, Brahmanbaria, Narsingdi, Savar, Tongi and Faridpur), and supports 115 user PCs in total (15 at HQ across 8 department VLANs and 5 per branch), plus wireless clients via 22 access points.

The scenario addresses a common enterprise problem: geographically separate offices need reliable connectivity, shared central services (DHCP, DNS, Web, Mail, FTP, NTP/Syslog), department-level segmentation and protection against unauthorized access, without the cost of dedicated servers at every branch. All shared services are hosted in the HQ server room, and WAN failures are handled automatically through dual WAN links and dynamic routing.

2. Project Objectives

Connectivity: interconnect the 20 branches and HQ over point-to-point WAN links using OSPF (single area, Area 0), with primary and backup paths for automatic re-routing.

Gateway redundancy: deploy HSRP on two Layer-3 core switches (HQ-CORE1 and HQ-CORE2) so HQ VLAN hosts keep their default gateway if one core switch fails.

Centralized services: provide DHCP (with relay agents at the branches), DNS, Web, Mail, FTP and NTP/Syslog from the HQ server room.

Network security: enforce departmental VLANs, extended ACLs, SSH-only device management, port security, NAT/PAT at the edge and an IPSec tunnel on a representative WAN link.

3. Proposed Network Components

Component

Approx. Number

Purpose

Router

22 (+1 ISP cloud)

2 HQ edge routers (HQ-EDGE-R1, HQ-EDGE-R2; NAT/PAT, IPSec) and 20 branch routers (BR01-R to BR20-R; gateway, OSPF, DHCP relay, ACLs, SSH)

Switch

24

2 Layer-3 core switches (HSRP, inter-VLAN routing, DHCP snooping), 2 HQ access switches (port security) and 20 branch access switches (port security, unused ports disabled)

PCs/Clients

115

15 HQ PCs across 8 department VLANs (Admin, Finance, HR, IT, Security/NOC, Management, Guest, Wireless) and 100 branch PCs (5 per branch x 20 branches)

Server

6

DHCP, DNS, FTP, Mail, Web and NTP/Syslog servers in the HQ server farm (VLAN 70)

Access Point

22

2 HQ APs (VLAN 90, WPA2-PSK) and 20 branch APs (1 per branch, WPA2-PSK, unique SSID/passphrase per location)

Other

1 cloud, cabling

ISP cloud to simulate the external Internet (NAT/PAT); copper/serial WAN links

4. Networking Concepts to be Used

Identify the Computer Networks concepts you expect to demonstrate:

☒ IP Addressing & Subnetting ☒ VLSM ☒ Routing

☒ DHCP ☒ DNS ☒ VLAN / Inter-VLAN Routing

☒ NAT ☒ ACL / Basic Security ☒ Wireless Networking

☒ Client–Server Communication ☒ Other: OSPF, HSRP, DHCP Relay, SSH, Port Security, IPSec VPN, NTP/Syslog, DHCP Snooping, WPA2-PSK Wireless, Extended ACLs, NAT/PAT

5. Preliminary Network Diagram

6. Proposed Tools

Cisco Packet Tracer will be the main simulation platform, used for topology building, device configuration (Cisco IOS CLI), server services and testing. Packet Tracer simulation mode will be used to inspect packets, and Microsoft Word / draw tools will be used for documentation and diagrams.

7. Expected Outcome

At the end of the project we expect to demonstrate a fully working HQ-and-twenty-branch network in which:

(a) all 20 branch and HQ hosts communicate with each other over OSPF-routed WAN links;

(b) branch PCs obtain IP addresses automatically from the central DHCP server through relay agents;

(c) users reach the intranet web portal, send and receive mail between branches, and download files over authenticated FTP using DNS names;

(d) the network survives failures, with HSRP switching the HQ gateway to HQ-CORE2 and OSPF re-routing traffic through backup WAN links;

(e) ACLs, SSH, port security, NAT/PAT and an IPSec tunnel protect the network, verified through a failure-recovery and application test matrix.

8. Initial Work Plan

Phase

Planned Activities

Approx. Time

Phase 1

Network design & research (topology, IP plan, VLAN and OSPF design)

2 days

Phase 2

Device configuration (HQ core with HSRP, BR01 and base device setup)

2 days

Phase 3

Routing/services implementation (OSPF, DHCP relay, DNS, Web, Mail, FTP; replicate BR02-BR20, wireless AP deployment at all 21 locations)

4days

Phase 4

Testing & troubleshooting (ACLs, SSH, NAT, IPSec, failure tests)

3 days

Phase 5

Finalization & presentation (report, demo preparation)

3 days

9. Division of Work

Group Member

Initial Responsibility

Partho Sarothi Ghosh (24549010089)

HQ design and configuration: core switches with HSRP, VLANs, HQ edge routers, NAT/PAT, and the server farm services (DHCP, DNS, Web, Mail, FTP, NTP/Syslog)

Aritry Talukdar (24549010069)

Branch and WAN design: 20 branch routers/switches, OSPF WAN links, DHCP relay, ACLs, SSH, port security, IPSec, wireless AP deployment (WPA2-PSK), and testing/documentation

10. References

Lab Demonstration

Cisco Systems, Cisco Packet Tracer documentation and Cisco IOS configuration guides (OSPF, HSRP, DHCP relay, ACL, IPSec).

ICE 2208 Computer Network Laboratory lecture and lab materials, Department of ICT, BUP.