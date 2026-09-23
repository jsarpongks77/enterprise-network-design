# Enterprise Network Design and Simulation

## Project Overview

This project focused on designing and simulating a dual-site enterprise network for GlobalBridge Consulting Ltd., a fictional organisation operating across Accra and Kumasi.

The project translated business and infrastructure requirements into a structured network design and validated the logical implementation using Cisco Packet Tracer.

The network used a hierarchical architecture and incorporated network segmentation, routing, access control, link redundancy, device security, network services, and inter-site connectivity.

## Project Objectives

- Design a hierarchical network architecture for the Accra and Kumasi sites
- Develop an IPv4 addressing and subnetting scheme
- Segment users and services using VLANs
- Enable controlled communication between network segments
- Implement routing within and between sites
- Apply access controls and baseline device security
- Introduce redundancy and availability measures
- Validate the logical network design in Cisco Packet Tracer
- Document the infrastructure and design decisions in a Technical Design Report

## Technologies and Concepts

- **Design & Simulation:** Cisco Packet Tracer, hierarchical network design
- **Addressing & Segmentation:** IPv4 addressing and subnetting, VLANs, 802.1Q trunking, inter-VLAN routing
- **Routing & Redundancy:** OSPF, EtherChannel
- **Services & Security:** DHCP and DHCP relay, Access Control Lists (ACLs), Cisco IOS device hardening
- **Inter-site Connectivity:** GRE tunnel


## Network Architecture

The network was designed to support two organisational sites in Accra and Kumasi using a hierarchical network architecture.

The design separated functions into core, distribution, and access layers, providing a structured approach to connectivity, segmentation, routing, security, and future expansion.

### Site Design

- **Accra:** Primary site supporting multiple user departments, network services, and enterprise connectivity
- **Kumasi:** Secondary site with its own local network infrastructure and connectivity to Accra
- **Inter-site connectivity:** A GRE tunnel provided logical connectivity between the two sites in the simulated environment

### Network Segmentation

VLANs were used to logically separate users and services into distinct network segments. This reduced broadcast domain size and provided a foundation for controlling communication between departments and services.

802.1Q trunk links carried multiple VLANs between network devices, while inter-VLAN routing enabled controlled communication between VLANs.

### Routing and Redundancy

OSPF was used for dynamic route exchange within the simulated network. EtherChannel combined multiple physical links into logical links, providing additional bandwidth and link redundancy.


## VLAN Design and IP Addressing

The IP addressing plan used Variable Length Subnet Masking (VLSM) to allocate address space based on the capacity requirements of each network segment. Subnets were sized to accommodate projected three-year growth while avoiding unnecessary address allocation.

### Accra Headquarters

| VLAN | Name | Network | Gateway | Capacity |
|---|---|---|---|---:|
| 40 | SALES | 10.10.0.0/23 | 10.10.0.1 | 510 |
| 90 | VOIP | 10.10.2.0/23 | 10.10.2.1 | 510 |
| 20 | FINANCE | 10.10.4.0/24 | 10.10.4.1 | 254 |
| 50 | ENGINEERING | 10.10.5.0/24 | 10.10.5.1 | 254 |
| 30 | HR | 10.10.6.0/25 | 10.10.6.1 | 126 |
| 10 | MGMT | 10.10.6.128/26 | 10.10.6.129 | 62 |
| 60 | EXEC | 10.10.6.192/27 | 10.10.6.193 | 30 |

### Kumasi Branch

| VLAN | Name | Network | Gateway | Capacity |
|---|---|---|---|---:|
| 70 | OPERATIONS | 10.20.0.0/24 | 10.20.0.1 | 254 |
| 72 | REGIONAL_SALES | 10.20.1.0/25 | 10.20.1.1 | 126 |
| 71 | FIELD_SUPPORT | 10.20.1.128/26 | 10.20.1.129 | 62 |

### Servers and Infrastructure

| VLAN | Name | Network | Gateway | Purpose |
|---|---|---|---|---|
| 80 | SERVERS | 172.16.0.0/24 | 172.16.0.1 | Server infrastructure |
| 99 | NATIVE/MGMT | 192.168.1.0/24 | 192.168.1.1 | Native/trunk management |

The addressing structure keeps the two sites logically separated while providing sufficient capacity for projected growth. Departmental VLANs also establish Layer 3 boundaries where communication between network segments can be controlled.
