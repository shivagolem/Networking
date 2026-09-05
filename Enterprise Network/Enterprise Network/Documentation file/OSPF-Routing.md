# OSPF Routing

## Overview

OSPF (Open Shortest Path First) is used as the dynamic routing protocol
in the routed portion of the enterprise network.

OSPF allows routers to dynamically learn routes to remote networks
without requiring every route to be configured manually.

## OSPF Process

The project uses:

- OSPF Process ID: 1
- Area: 0

## Router IDs

| Device | OSPF Router ID |
|---|---|
| R2 | 2.2.2.2 |
| R3 | 3.3.3.3 |
| R4 | 4.4.4.4 |

## OSPF Networks

### R2

R2 advertises the following networks into OSPF:

```text
10.0.0.0/30
10.0.0.4/30
10.0.0.8/30
10.0.0.12/30
10.0.0.16/30