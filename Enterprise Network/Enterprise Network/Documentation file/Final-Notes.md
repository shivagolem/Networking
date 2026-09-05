# Final Project Notes

## Project Summary

This project demonstrates the configuration of a small enterprise
network using Cisco networking technologies.

The network was designed with multiple departments, branch networks,
Layer 2 switches, Layer 3 switches, and routers.

## Technologies Implemented

- IPv4 addressing
- VLANs
- Access ports
- Trunk links
- Layer 3 switching
- OSPF dynamic routing
- Spanning Tree Protocol
- PortFast
- Network verification and troubleshooting

## Network Segmentation

The enterprise network uses separate VLANs for different departments:

- VLAN 10 - Sales
- VLAN 20 - HR
- VLAN 30 - IT
- VLAN 40 - Finance

This provides logical separation between departments and makes the
network easier to manage.

## Routing

OSPF is used to dynamically exchange routes between the routed network
devices.

This reduces the need for manually configuring every remote route and
allows the network to adapt when routing information changes.

## Branch Connectivity

The topology includes two branch networks:

- Branch 1 - 192.168.110.0/24
- Branch 2 - 192.168.120.0/24

The branches connect to the HQ network through the routing
infrastructure.

## Verification

The network configuration was verified using Cisco IOS commands
including:

```text
show ip interface brief
show vlan brief
show interfaces trunk
show ip route
show ip ospf neighbor
show ip protocols
show running-config
ping
traceroute