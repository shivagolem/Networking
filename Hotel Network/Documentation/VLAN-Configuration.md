
---

# 3. `VLAN-Configuration.md`

```markdown
# VLAN Configuration

## Overview

VLANs are used to logically separate different departments of the hotel.

Each VLAN represents a separate network.

## VLANs Used

| VLAN ID | Network | Department |
|---|---|---|
| 10 | 192.168.1.0/24 | IT |
| 20 | 192.168.2.0/24 | Admin |
| 30 | 192.168.3.0/24 | Sales |
| 40 | 192.168.4.0/24 | HR |
| 50 | 192.168.5.0/24 | Finance |
| 60 | 192.168.6.0/24 | Logistics |
| 70 | 192.168.7.0/24 | Store |
| 80 | 192.168.8.0/24 | Reception |

## VLAN Purpose

VLANs help separate departments and reduce unnecessary broadcast traffic.

They also make the network easier to manage and provide a foundation for applying security policies between departments.

## Inter-VLAN Routing

Router-on-a-Stick is used for inter-VLAN routing.

The router interface connected to the switch is configured with multiple subinterfaces.

Each subinterface is associated with a VLAN using 802.1Q encapsulation.

Example:

```text
interface FastEthernet0/0.10
 encapsulation dot1Q 10
 ip address 192.168.1.1 255.255.255.0