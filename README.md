# Network-Configuration-Project

This project simulates a network topology for a corporate enterprise using a 3-layer model: Core, Distribution, and Access. The network is built using various devices such as Routers, Layer 2/3 Switches, and Multi-layer Switches (MLS). The primary goal of the simulation is to demonstrate the configuration of routing protocols, VLANs, and inter-VLAN routing in a typical business network environment.

## Network Architecture

- **Core Layer**: A Layer 3 Router performing inter-VLAN routing and connecting the internal network to external networks (Internet).
- **Distribution Layer**: Layer 3 or Layer 2 Switches, which aggregate traffic from the Access Layer and route it to the Core Layer.
- **Access Layer**: Layer 2 Switches (or Multi-layer Switches), which provide connectivity for end devices like PCs, Laptops, and other networked devices. VLANs are configured on this layer to segment network traffic for various departments.

## Project Features

- **Routing Protocols**: Configuration of OSPF for dynamic routing across the network.
- **VLAN Configuration**: Segment the network using VLANs and set up inter-VLAN routing using Multi-layer Switches.
- **DHCP Setup**: Automatic IP address assignment for end devices using a DHCP server.
- **Security Features**: Implementing basic security measures using Access Control Lists (ACLs) to restrict traffic flow between VLANs.

## Goal

This simulation helps in understanding enterprise-level networking principles and provides a practical example for network engineers and students to learn from.
