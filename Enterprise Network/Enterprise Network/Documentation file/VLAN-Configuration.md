# VLAN Configuration

## Overview

VLANs are used to logically separate different departments within the
enterprise network.

Each department is assigned a dedicated VLAN.

## VLAN Table

| VLAN ID | Department | Network |
|---|---|---|
| 10 | SALES | 192.168.10.0/24 |
| 20 | HR | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |
| 40 | FINANCE | 192.168.40.0/24 |

## Department Switches

| Switch | Department | VLAN |
|---|---|---|
| SW1 | Sales | VLAN 10 |
| SW2 | HR | VLAN 20 |
| SW3 | IT | VLAN 30 |
| SW4 | Finance | VLAN 40 |
| SW5 | Branch 1 | VLAN 10 |
| SW6 | Branch 2 | VLAN 10 |

## Access Ports

Access ports are used to connect end devices such as PCs to their
respective VLAN.

Examples:

```text
SW1 → Sales PCs → VLAN 10
SW2 → HR PCs → VLAN 20
SW3 → IT PCs → VLAN 30
SW4 → Finance PCs → VLAN 40