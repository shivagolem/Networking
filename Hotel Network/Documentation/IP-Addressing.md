# IP Addressing

## Overview

Private IPv4 addressing is used throughout the hotel network.

Each VLAN is assigned a separate /24 network.

## VLAN Networks

| VLAN | Network | Default Gateway |
|---|---|---|
| VLAN 10 | 192.168.1.0/24 | 192.168.1.1 |
| VLAN 20 | 192.168.2.0/24 | 192.168.2.1 |
| VLAN 30 | 192.168.3.0/24 | 192.168.3.1 |
| VLAN 40 | 192.168.4.0/24 | 192.168.4.1 |
| VLAN 50 | 192.168.5.0/24 | 192.168.5.1 |
| VLAN 60 | 192.168.6.0/24 | 192.168.6.1 |
| VLAN 70 | 192.168.7.0/24 | 192.168.7.1 |
| VLAN 80 | 192.168.8.0/24 | 192.168.8.1 |

## Router-to-Router Links

The routers use /30 networks for point-to-point serial connections.

| Network | Purpose |
|---|---|
| 10.10.10.0/30 | Router-to-router link |
| 10.10.10.4/30 | Router-to-router link |
| 10.10.10.8/30 | Router-to-router link |

## DHCP

DHCP is configured on the routers to automatically provide IP addresses to end devices.

The first 20 addresses of each network are excluded from the DHCP pools for gateway and reserved addresses.

DNS server:

```text
8.8.8.8