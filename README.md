# Dynamic Routing Using RIP Version 2

## Project Overview

This project demonstrates the implementation of Dynamic Routing using Routing Information Protocol Version 2 (RIPv2) in Cisco Packet Tracer.

The network consists of three Cisco routers connected through serial links, with each router serving a separate LAN. RIPv2 is configured to exchange routing information automatically and allow communication between devices across different networks.

The project focuses on router interface configuration, serial connectivity, dynamic route advertisement, routing-table analysis, and end-to-end connectivity testing.

## Learning Objectives

- Understand the fundamentals of dynamic routing.
- Understand the operation of RIP Version 2.
- Configure router Ethernet and serial interfaces.
- Establish communication between multiple routers.
- Configure RIPv2 on all three routers.
- Verify dynamically learned routes.
- Test communication between different LAN networks.
- Troubleshoot routing and interface connectivity.

## Network Topology

The network consists of:

- 3 Cisco 2911 routers (R1, R2 and R3)
- 3 Cisco 2960 switches
- 6 PCs (2 PCs per LAN)
- Serial connections between routers
- Three separate LAN networks

## IP Addressing Plan

### Router LAN Interfaces

| Router | Interface | IP Address | Subnet Mask |
|---|---|---|---|
| R1 | F0/0 | 192.168.10.1 | 255.255.255.0 |
| R2 | F0/0 | 192.168.20.1 | 255.255.255.0 |
| R3 | F0/0 | 192.168.30.1 | 255.255.255.0 |

### Serial Connections

| Connection | Interface | IP Address | Subnet Mask |
|---|---|---|---|
| R1 - R2 | R1 Se2/0 | 192.168.40.1 | 255.255.255.252 |
| R1 - R2 | R2 Se2/0 | 192.168.40.2 | 255.255.255.252 |
| R2 - R3 | R2 Se3/0 | 192.168.50.1 | 255.255.255.252 |
| R2 - R3 | R3 Se3/0 | 192.168.50.2 | 255.255.255.252 |

### PC Addressing

| PC | IP Address | Subnet Mask | Default Gateway |
|---|---|---|---|
| PC0 | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 |
| PC1 | 192.168.10.11 | 255.255.255.0 | 192.168.10.1 |
| PC2 | 192.168.20.10 | 255.255.255.0 | 192.168.20.1 |
| PC3 | 192.168.20.11 | 255.255.255.0 | 192.168.20.1 |
| PC4 | 192.168.30.10 | 255.255.255.0 | 192.168.30.1 |
| PC5 | 192.168.30.11 | 255.255.255.0 | 192.168.30.1 |

## Dynamic Routing Protocol

### RIP Version 2

RIPv2 is configured on all three routers to exchange routing information and automatically learn remote networks.

RIPv2 supports:
- Classless routing
- Variable Length Subnet Masking (VLSM)
- Classless Inter-Domain Routing (CIDR)
- Route advertisements using multicast address 224.0.0.9
- Hop-count-based route selection

The maximum usable hop count is 15.

## Implementation Tasks

1. Build the three-router network topology.
2. Configure LAN interface IP addresses.
3. Configure serial interface IP addresses.
4. Check serial interfaces and identify DCE connections.
5. Configure clock rates on DCE interfaces where required.
6. Enable the router interfaces.
7. Configure IP addresses and default gateways on all PCs.
8. Configure RIP Version 2 on R1, R2 and R3.
9. Verify routing protocol operation.
10. Inspect the routing tables for dynamically learned routes.
11. Test communication within the same LAN.
12. Test communication between different LANs.

## Verification Commands

### Interface Verification

```bash
show ip interface brief
```

### Serial Interface Verification

```bash
show controllers serial 2/0
```

### RIP Configuration Verification

```bash
show ip protocols
```

### Routing Table Verification

```bash
show ip route
```

### Connectivity Testing

```bash
ping 192.168.20.10
ping 192.168.30.10
```

## Expected Routing Table Codes

| Code | Meaning |
|---|---|
| C | Connected route |
| L | Local route |
| R | RIP-learned route |
| S | Static route |
| O | OSPF-learned route |
| D | EIGRP-learned route |

Routes marked with `R` indicate networks learned through RIP.

## Connectivity Testing

The following tests are performed:

- Communication between PCs within the same LAN.
- Communication between PCs in different LANs.
- Verification of remote network routes on all three routers.
- Verification of router interface status and serial connectivity.

## Technologies and Concepts

- Cisco Packet Tracer
- Cisco 2911 Routers
- Cisco 2960 Switches
- Dynamic Routing
- Routing Information Protocol Version 2 (RIPv2)
- IPv4 Addressing and Subnetting
- Serial WAN Connections
- DCE and DTE
- Routing Table Analysis
- ICMP Connectivity Testing
- Network Troubleshooting

## Key Learning Outcomes

- Understand how dynamic routing protocols exchange network information.
- Configure RIPv2 on multiple routers.
- Establish serial communication between routers.
- Understand routing metrics and hop-count-based path selection.
- Identify dynamically learned routes in routing tables.
- Troubleshoot routing and connectivity problems.

## Repository Contents

- Cisco Packet Tracer topology file
- Network topology screenshots
- Router interface configuration evidence
- Serial connection verification screenshots
- RIP configuration screenshots
- Routing table screenshots
- Connectivity test screenshots
- Completed practical lab report
