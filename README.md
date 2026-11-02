# Enterprise Campus Network — Cisco Packet Tracer

A Cisco Packet Tracer enterprise campus network lab with redundant multilayer core switches, VLAN segmentation, inter-VLAN routing, DHCP services, gateway redundancy, switching resiliency, access controls, and simulated Internet access.

## Project files

| File | Description |
|---|---|
| `Enterprise-Campus-Network.pkt` | Cisco Packet Tracer topology and device configuration |
| `Configuration-Runbook.pdf` | 28-page step-by-step rebuild guide, addressing plan, device configurations, verification commands, and troubleshooting |

## Technologies and features

- VLANs: 10 Management, 20 Faculty, 30 Students, 40 Guests, 50 Servers, 60 CCTV/IoT, 70 Voice
- Cisco 3560 multilayer core switches and Cisco 2960 access switches
- Inter-VLAN routing using SVIs
- HSRP for default-gateway redundancy
- 802.1Q trunk links
- LACP EtherChannel between the core switches
- Rapid PVST+ spanning tree
- DHCP pools and DHCP relay (`ip helper-address`)
- Extended ACLs for student and guest traffic restrictions
- SSH v2 for remote device management
- Port Security with sticky MAC learning
- Static routing, default routing, and floating backup route
- NAT/PAT for simulated Internet access
- Server services: DHCP, DNS, HTTP/HTTPS, and FTP

## VLAN and gateway plan

| VLAN | Name | Network | HSRP virtual gateway |
|---:|---|---|---|
| 10 | MANAGEMENT | `10.10.10.0/24` | `10.10.10.1` |
| 20 | FACULTY | `10.10.20.0/24` | `10.10.20.1` |
| 30 | STUDENTS | `10.10.30.0/24` | `10.10.30.1` |
| 40 | GUESTS | `10.10.40.0/24` | `10.10.40.1` |
| 50 | SERVERS | `10.10.50.0/24` | `10.10.50.1` |
| 60 | CCTV-IOT | `10.10.60.0/24` | `10.10.60.1` |
| 70 | VOICE | `10.10.70.0/24` | `10.10.70.1` |

## Main devices

- Routers: `R1`, `ROUTER-ISP`
- Core switches: `CORE-SW1`, `CORE-SW2`
- Access switches: `ACCESS-SW1` through `ACCESS-SW6`
- Server switches: `SERVER-ACCESS-SW`, `SERVER-SW`
- Servers: `Server1`, `Server2`, `Server3` (and optional `Server0`)

## How to open the project

1. Install and open Cisco Packet Tracer.
2. Download `Enterprise-Campus-Network.pkt`.
3. Open it in Packet Tracer.
4. Refer to `Configuration-Runbook.pdf` for the topology map, IP plan, configuration blocks, and test commands.

## Verification

The runbook includes commands and tests such as:

```text
show vlan brief
show interfaces trunk
show cdp neighbors
show spanning-tree vlan 30
show etherchannel summary
show standby brief
show ip interface brief
show ip route
show access-lists
show ip nat translations
show port-security address
```

It also documents DHCP, DNS, web, FTP, SSH, HSRP failover, and simulated ISP reachability tests.

## Important before making the repository public

- Review the Packet Tracer file for saved passwords, usernames, and other credentials.
- The PDF contains an example lab SSH credential (`netadmin` / `NetLab@123`). Replace it or remove it from any public copy; never reuse it outside this lab.
- Confirm that the `.pkt` file opens correctly and that the final topology/configuration is the version you intend to publish.
- Add screenshots of the topology and successful verification outputs if you want the repository to be easier for recruiters to review.

## Notes

This is a Packet Tracer learning project. The ISP side uses a simulated loopback target rather than a real Internet connection. See the PDF for documented implementation details and rebuild caveats.
