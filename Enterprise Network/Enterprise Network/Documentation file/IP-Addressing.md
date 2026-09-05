# IP Addressing

## Overview

The network uses IPv4 addressing. Point-to-point router links use /30
subnets, while LAN and VLAN networks use /24 subnets.

## Router-to-Router / Routed Links

| Device | Interface | IP Address | Subnet Mask |
|---|---|---|---|
| R1 | Serial0/0/0 | 10.0.0.1 | 255.255.255.252 |
| R2 | Serial0/0/1 | 10.0.0.2 | 255.255.255.252 |
| R2 | Serial0/0/0 | 10.0.0.5 | 255.255.255.252 |
| R3 | Serial0/0/1 | 10.0.0.6 | 255.255.255.252 |
| R2 | Serial0/2/0 | 10.0.0.9 | 255.255.255.252 |
| R4 | Serial0/0/0 | 10.0.0.10 | 255.255.255.252 |

## HQ Routed Link

| Device | Interface | IP Address | Subnet Mask |
|---|---|---|---|
| R2 | FastEthernet0/0 | 10.0.0.13 | 255.255.255.252 |
| R2 | FastEthernet0/1 | 10.0.0.17 | 255.255.255.252 |
| MLS1 | FastEthernet0/1 | 10.0.0.14 | 255.255.255.252 |

## VLAN Networks

| VLAN ID | Department | Network |
|---|---|---|
| 10 | SALES | 192.168.10.0/24 |
| 20 | HR | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |
| 40 | FINANCE | 192.168.40.0/24 |

## Branch Networks

| Branch | Network |
|---|---|
| Branch 1 | 192.168.110.0/24 |
| Branch 2 | 192.168.120.0/24 |

## Addressing Notes

- /30 subnets are used for point-to-point routed connections.
- /24 subnets are used for LAN/VLAN networks.
- VLANs provide logical network segmentation between departments.
- Layer 3 devices provide routing between different IP networks.