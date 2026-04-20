# networking
Enterprise network simulation with VLANs, inter-VLAN routing, DHCP multi-scope, and guest network isolation (Cisco Packet Tracer)
#
# Enterprise Network Infrastructure – Cisco Packet Tracer

This project simulates the network infrastructure of a manufacturing company, designed to ensure secure communication between departments and reliable connectivity to external resources.

## Overview

The network is divided into multiple departments using VLAN segmentation to improve performance and security. Inter-VLAN communication, centralized DHCP, DNS resolution, and controlled internet access are fully implemented.

## Network Architecture

### VLANs and Subnets
- VLAN 10 – Warehouse: 192.168.10.0/24
- VLAN 20 – Administration: 192.168.20.0/24
- VLAN 30 – Marketing: 192.168.30.0/24
- Guest Network: 192.168.105.192/26 (isolated)

### Core Components
- Layer 3 Switch (SWITCH01) for inter-VLAN routing
- Router (ROUTER01) for internal network management
- Router (ROUTER02) for external network (internet simulation)
- Multiple web servers (internal + external)

## Key Features

- VLAN segmentation for department isolation
- Inter-VLAN routing using Layer 3 switch
- Centralized DHCP server with multi-scope configuration
- DHCP relay configured via `ip helper-address`
- Dynamic routing using RIP protocol
- DNS configuration for internal domain resolution
- Simulated internet access through external server
- Guest network fully isolated from internal resources

## Security Implementation

- Standard ACL configured on router to isolate guest network:
  - Blocks access to internal VLANs
  - Allows internet-only access
- Logical segmentation through VLANs

## Technologies Used

- Cisco Packet Tracer
- TCP/IP Networking
- VLANs and Subnetting
- Routing (RIP)
- DHCP (multi-scope + relay)
- DNS configuration
- Access Control Lists (ACLs)

## Project Files

- `.pkt` file: full network simulation
- Documentation: detailed network design and configuration

## Key Learning Outcomes

- Design and implementation of VLAN-based network architecture
- Configuration of inter-VLAN routing
- DHCP relay and multi-network IP management
- Network security through ACLs and segmentation
- Implementation of dynamic routing protocols (RIP)
- DNS configuration and name resolution
- Troubleshooting connectivity across multiple network layers

## Future Improvements

- Implementation of extended ACLs for protocol-based filtering
- Port Security for access control at switch level
- SSH configuration for secure device management
- DHCP Snooping to prevent unauthorized DHCP servers
- Network redundancy and failover mechanisms

## Author

Andrea Coppola
