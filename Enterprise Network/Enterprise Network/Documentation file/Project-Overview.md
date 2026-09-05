# Enterprise Network Configuration

## Project Overview

This project demonstrates the design and configuration of an enterprise
network using Cisco routers, Layer 2 switches, and Layer 3 multilayer switches.

The network contains multiple departments and branch locations.
VLANs are used to separate departments, while routing and OSPF are used
to provide communication between different network segments.

## Devices Used

### Routers
- R1 - ISP
- R2 - HQ
- R3 - Branch 1
- R4 - Branch 2

### Switches
- SW1 - Sales
- SW2 - HR
- SW3 - IT
- SW4 - Finance
- SW5 - Branch 1
- SW6 - Branch 2

### Layer 3 Switches
- MLS1 - HQ
- MLS2 - HQ

## VLANs

| VLAN ID | Department |
|---------|------------|
| 10 | SALES |
| 20 | HR |
| 30 | IT |
| 40 | FINANCE |

## Technologies Used

- Cisco IOS
- VLANs
- Access Ports
- Trunk Ports
- Inter-VLAN Routing
- Layer 3 Switching
- OSPF
- IPv4 Addressing
- Spanning Tree Protocol
- PortFast

## Project Objectives

1. Design an enterprise network topology.
2. Configure routers and switches.
3. Configure IPv4 addressing.
4. Create and assign VLANs.
5. Configure trunk links.
6. Configure Layer 3 routing.
7. Configure OSPF dynamic routing.
8. Verify connectivity between network devices.
9. Troubleshoot network configuration issues.
10. Document the complete network configuration.

## Verification

The configuration is verified using Cisco IOS commands such as:

show ip interface brief
show vlan brief
show interfaces trunk
show ip route
show ip ospf neighbor
show running-config
ping
traceroute