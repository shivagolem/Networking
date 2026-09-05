# Router Configuration

## Overview

Four routers are used in the enterprise topology:

- R1 - ISP
- R2 - HQ
- R3 - Branch 1
- R4 - Branch 2

The routers provide connectivity between the different network segments.

## R1 - ISP

R1 is connected to R2 using a point-to-point serial connection.

```text
R1 Serial0/0/0
IP Address: 10.0.0.1/30