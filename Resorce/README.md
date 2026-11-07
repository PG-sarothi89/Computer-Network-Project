# GlobalTech Industries Ltd. - Secure Multi-Branch Enterprise Network
## Cisco Packet Tracer Project | BUP ICE 2208 Computer Network Laboratory

### Project Title
**Secure Multi-Branch Enterprise Network WAN Simulation for GlobalTech Industries Ltd.**

### Team
| Member | ID | Role |
|--------|-----|------|
| Partho Sarothi Ghosh | 24549010089 | HQ Design: Core switches, HSRP, Edge routers, NAT/PAT, Server farm |
| Aritry Talukdar | 24549010069 | Branch/WAN Design: 20 branch configs, OSPF, DHCP relay, ACLs, Security |

### Supervisor
**Sharmeen Jahan Seema** - Lecturer, Department of ICT, FST, Bangladesh University of Professionals

---

### Network Scale
| Component | Count |
|-----------|-------|
| Regional Branches | 20 |
| HQ Layer-3 Core Switches (HSRP) | 2 |
| HQ Edge Routers (WAN/NAT/IPSec) | 2 |
| Branch Routers | 20 |
| HQ Access Switches | 2 |
| Branch Access Switches | 20 |
| HQ Servers | 6 |
| Wired PCs (HQ) | 15 |
| Wired PCs (Branches) | 100 (5 per branch) |
| Wireless Access Points | 22 (2 HQ + 20 branches) |
| **Total Wired PCs** | **115** |
| **Total Devices** | **190+** |

### Directory Structure
```
GlobalTech_CN_Project/
|-- configs/
|   |-- HQ/
|   |   |-- HQ-CORE1.cfg          (L3 switch, HSRP active, OSPF)
|   |   |-- HQ-CORE2.cfg          (L3 switch, HSRP standby, OSPF)
|   |   |-- HQ-EDGE-R1.cfg        (Primary WAN, NAT/PAT, IPSec)
|   |   |-- HQ-EDGE-R2.cfg        (Secondary WAN, backup links)
|   |   |-- HQ-ACCESS-SW1.cfg     (Admin/Finance/HR/Servers)
|   |   |-- HQ-ACCESS-SW2.cfg     (IT/NOC/Mgmt/Guest/Wireless)
|   |   |-- SERVER-SERVICES-SETUP.txt
|   |-- Branches/
|   |   |-- BR01-R.cfg ... BR20-R.cfg   (20 branch routers)
|   |   |-- BR01-SW.cfg ... BR20-SW.cfg (20 branch switches)
|   |-- WAN/
|   |   |-- WAN-TOPOLOGY-OVERVIEW.txt
|   |-- Wireless/
|       |-- WIRELESS-AP-SETUP-GUIDE.txt
|-- docs/
|   |-- Project_Proposal_GlobalTech_BUP.docx
|   |-- IP_ADDRESSING_TABLE.txt
|   |-- SECURITY_POLICY.txt
|   |-- GlobalTech_Multibranch_Cisco_Project_Master_Plan.txt
|-- diagrams/
|   |-- bup_logo.png
|   |-- preliminary_network_diagram.png
|-- README.md
```

### Key Technologies Demonstrated
- [x] IP Addressing & Subnetting (VLSM /24 and /30)
- [x] OSPF Dynamic Routing (Area 0, 20+ neighbors)
- [x] HSRP Gateway Redundancy (Active/Standby core switches)
- [x] VLANs & Inter-VLAN Routing (9 HQ VLANs)
- [x] Central DHCP with Relay Agents (20 branch pools)
- [x] DNS (6 internal A records)
- [x] NAT/PAT (Internet access translation)
- [x] IPSec VPN (Site-to-site tunnel, BR01-HQ)
- [x] Extended ACLs (Branch + Guest security policies)
- [x] SSH-Only Management (RSA 2048, Telnet disabled)
- [x] Port Security (Sticky MAC, violation restrict/shutdown)
- [x] Wireless Networking (WPA2-PSK, 22 APs)
- [x] NTP/Syslog Monitoring (Centralized logging)
- [x] WAN Redundancy (Dual links for BR01-BR05, OSPF failover)
- [x] DHCP Snooping (Rogue DHCP prevention)
- [x] Client-Server Communication (FTP, Email, Web)

### Quick Start
1. Open Cisco Packet Tracer 8.x
2. Build the topology following `WAN-TOPOLOGY-OVERVIEW.txt`
3. Configure HQ devices first (CORE1 -> CORE2 -> EDGE-R1 -> EDGE-R2 -> Switches)
4. Set up servers following `SERVER-SERVICES-SETUP.txt`
5. Configure branches (paste BR01-R.cfg into CLI, then BR01-SW.cfg, etc.)
6. Set up wireless APs following `WIRELESS-AP-SETUP-GUIDE.txt`
7. Test connectivity: branch PC -> ping www.globaltech.local
