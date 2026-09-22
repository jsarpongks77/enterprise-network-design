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
