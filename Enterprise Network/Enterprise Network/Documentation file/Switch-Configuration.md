# Switch Configuration

## Overview

The project uses six Layer 2 switches and two Layer 3 multilayer
switches.

The Layer 2 switches provide VLAN-based network access for end devices,
while the Layer 3 switches provide routing functionality within the
HQ network.

## Layer 2 Switches

| Switch | Location / Department | VLAN |
|---|---|---|
| SW1 | Sales | VLAN 10 |
| SW2 | HR | VLAN 20 |
| SW3 | IT | VLAN 30 |
| SW4 | Finance | VLAN 40 |
| SW5 | Branch 1 | VLAN 10 |
| SW6 | Branch 2 | VLAN 10 |

## VLAN Configuration

The main HQ VLANs are:

```text
VLAN 10 - SALES
VLAN 20 - HR
VLAN 30 - IT
VLAN 40 - FINANCE