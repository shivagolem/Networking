
---

# 5. `OSPF-Routing.md`

```markdown
# OSPF Routing

## Overview

Open Shortest Path First (OSPF) is used as the dynamic routing protocol in the hotel network.

All routers participate in OSPF Area 0.

## Router IDs

| Router | Router ID |
|---|---|
| R1 | 3.3.3.3 |
| R2 | 2.2.2.2 |
| R3 | 1.1.1.1 |

## OSPF Configuration

### R1

```text
router ospf 1
 router-id 3.3.3.3
 network 192.168.6.0 0.0.0.255 area 0
 network 192.168.7.0 0.0.0.255 area 0
 network 192.168.8.0 0.0.0.255 area 0
 network 10.10.10.4 0.0.0.3 area 0
 network 10.10.10.8 0.0.0.3 area 0
 network 10.10.10.0 0.0.0.3 area 0

R2

router ospf 1
 router-id 2.2.2.2
 network 192.168.3.0 0.0.0.255 area 0
 network 192.168.4.0 0.0.0.255 area 0
 network 192.168.5.0 0.0.0.255 area 0
 network 10.10.10.0 0.0.0.3 area 0
 network 10.10.10.8 0.0.0.3 area 0

R3

router ospf 1
 router-id 1.1.1.1
 network 192.168.1.0 0.0.0.255 area 0
 network 192.168.2.0 0.0.0.255 area 0
 network 10.10.10.0 0.0.0.3 area 0
 network 10.10.10.4 0.0.0.3 area 0
 network 10.10.10.8 0.0.0.3 area 0

OSPF Verification


show ip ospf neighbor
show ip route
show ip protocols