# Cisco Packet Tracer Network Project

This repository contains a Cisco Packet Tracer network simulation project (`network-simulation-project.pkt`) and a detailed project report in Polish (`sprawozdanie.pdf`).

## Overview

The project involves designing, configuring, and testing a computer network in a simulated environment. The key objectives include:
- Implementing dynamic routing with OSPF (including MD5 authentication).
- Configuring DHCP servers for IP address allocation.
- Creating a scalable network to support:
  - **500 hosts** in one segment.
  - **5000 hosts** in another segment.
- Verifying connectivity and ensuring the network meets performance and scalability requirements.

## Network Topology

The network consists of:
- **3 Routers** (R1, R2, R3).
- **2 Switches** (S1, S2).
- Two large segments with proper IP subnetting to accommodate the required number of hosts.

### Key IP Addressing:
| Device | Interface  | IP Address       | Subnet Mask        |
|--------|------------|------------------|--------------------|
| R1     | g0/0       | 172.16.1.254     | 255.255.254.0 (/23)|
| R1     | s0/1/0     | 203.0.113.1      | 255.255.255.252 (/30)|
| R2     | s0/1/0     | 203.0.113.2      | 255.255.255.252 (/30)|
| R2     | s0/1/1     | 198.51.100.1     | 255.255.255.252 (/30)|
| R3     | g0/0       | 192.168.159.254  | 255.255.224.0 (/19)|
| R3     | s0/1/1     | 198.51.100.2     | 255.255.255.252 (/30)|

## Features and Configuration

1. **Dynamic Routing (OSPF)**:
   - Configured OSPF across routers.
   - Authentication using MD5 for enhanced security.
   - Verified neighbor relationships and routing protocol configuration.

2. **DHCP Configuration**:
   - Implemented DHCP on R1 and R3 for dynamic IP allocation.
   - Reserved key addresses to avoid conflicts with network devices.

3. **Switch Configuration**:
   - Configured VLAN interfaces with appropriate IPs.
   - Configured trunk and access ports.

4. **Subnetting**:
   - Subnet mask `/23` used for 500-host segment (provides 510 usable addresses).
   - Subnet mask `/19` used for 5000-host segment (provides 8190 usable addresses).

## Files

- **`network-simulation-project.pkt`**: The Cisco Packet Tracer file containing the network simulation.
- **`sprawozdanie.pdf`**: A detailed project report (in Polish) documenting the design, configuration, and testing process.

## How to Open the Project

1. Install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) (version used: 8.0 or higher).
2. Open the `.pkt` file in Cisco Packet Tracer.
3. Review the network topology and device configurations.

## Report Highlights

The report includes:
- Step-by-step configuration processes.
- Troubleshooting insights (e.g., resolving DHCP and OSPF authentication issues).
- Validation of network functionality through ping tests and protocol verification.
- Subnetting and IP address assignment rationale.

## Conclusions

This project demonstrates practical knowledge in:
- Designing scalable networks.
- Configuring routers, switches, and network protocols.
- Implementing secure and efficient routing using OSPF with MD5 authentication.
- Troubleshooting and resolving network configuration issues.

## Author

- **Krakasevich Aleksandr**  
  Academic Project supervised by: **Dr. hab. inż. Radosław Wróbel**

---

For any questions or issues, please open an issue in this repository.
