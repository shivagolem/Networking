# Campus Network Project

This is my Cisco Packet Tracer campus network project.

I created this project to practice how an enterprise network works. I used VLANs to separate different departments and used two multilayer switches for gateway backup.

## Devices used

- 2 Cisco 2811 routers
- 2 Cisco 3560 multilayer switches
- 6 Cisco 2960 access switches
- 2 Cisco 2960 server switches
- PCs, laptops, printers, access points, IP phones, cameras and servers

## VLAN details

| VLAN | Name | Network | Gateway |
|---|---|---|---|
| 10 | Management | 10.10.10.0/24 | 10.10.10.1 |
| 20 | Faculty | 10.10.20.0/24 | 10.10.20.1 |
| 30 | Students | 10.10.30.0/24 | 10.10.30.1 |
| 40 | Guests | 10.10.40.0/24 | 10.10.40.1 |
| 50 | Servers | 10.10.50.0/24 | 10.10.50.1 |
| 60 | CCTV-IoT | 10.10.60.0/24 | 10.10.60.1 |
| 70 | Voice | 10.10.70.0/24 | 10.10.70.1 |

## Server IP addresses

- Server1: 10.10.50.10 (DHCP and DNS)
- Server2: 10.10.50.20 (Web server)
- Server3: 10.10.50.30 (FTP server)
- Server0: 10.10.50.40 (optional server)

## Technologies used

- VLAN and inter-VLAN routing
- Trunking (802.1Q)
- HSRP for gateway redundancy
- EtherChannel using LACP
- Rapid PVST+ spanning tree
- DHCP and DHCP relay
- DNS, HTTP and FTP services
- ACL for traffic restriction
- SSH for remote access
- Port Security
- Static routing and default routing
- NAT/PAT

## Project files

- `Campus-Network.pkt` - Packet Tracer project
- `Configuration.txt` - Main device configuration commands
- `Configuration-Runbook.pdf` - Detailed step-by-step configuration and testing guide

## How to open

1. Open Cisco Packet Tracer.
2. Open `Campus-Network.pkt`.
3. Check the topology and device connections.
4. Use `Configuration.txt` and the PDF when you want to understand or configure the devices again.

This is a learning project made using Cisco Packet Tracer.
