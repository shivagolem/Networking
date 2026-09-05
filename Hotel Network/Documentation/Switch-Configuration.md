
---

# 6. `Switch-Configuration.md`

```markdown
# Switch Configuration

## Overview

Cisco switches are used to connect end devices and provide VLAN connectivity.

The switches are configured with VLANs and trunk links where required.

## VLANs

The switches use the following VLAN IDs:

```text
10
20
30
40
50
60
70
80

Access Ports

interface FastEthernet0/1
 switchport mode access
 switchport access vlan 10


Trunk Ports

interface FastEthernet0/24
 switchport mode trunk

Verification Commands

show vlan brief
show interfaces trunk
show spanning-tree
show running-config