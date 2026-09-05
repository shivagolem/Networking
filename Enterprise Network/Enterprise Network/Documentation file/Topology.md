# Network Topology

## Overview

The network is divided into an HQ network and two branch networks.

The enterprise topology consists of:

- 4 routers
- 6 Layer 2 switches
- 2 Layer 3 multilayer switches
- Multiple end-user PCs

## Router Connectivity

```text
R1 - ISP
   |
   | 10.0.0.0/30
   |
R2 - HQ
   |
   +---------------- R3 - Branch 1
   |
   +---------------- R4 - Branch 2