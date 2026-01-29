# Network Configuration Project

This project simulates a network topology for a corporate enterprise using a 3-layer model: Core, Distribution, and Access. It includes configuration of routing protocols, VLANs, inter-VLAN routing, and more.

## Network Devices Configured:
- **Core Routers**: Core_1, Core_2
- **Access Routers**: Router_DMZ
- **ISP Router**: ISP

## Project Features
- **OSPF Configuration** for dynamic routing
- **VLAN Configuration** for network segmentation
- **DHCP Setup** for automatic IP address assignment
- **Basic Security** using **ACLs**

## Folder Structure
- `configs/`: Contains all configuration files for routers and switches
- `images/`: Contains network topology diagrams

## How to Use
1. Clone the repository.
2. Load the configuration files on appropriate network devices.
3. Implement the setup and test the network.


## Network Topology

### Network Topology Diagram
This diagram shows the full enterprise network using a 3-tier architecture
(Core – Distribution – Access), including DMZ and ISP connectivity.

![Network Topology Diagram 1](images/network_topology1.png)
![Network Topology Diagram 2](images/network_topology2.png)

## Wireless Network

The wireless network is centrally managed by a Wireless LAN Controller (WLC),
supporting secure enterprise authentication and controlled guest access.

📄 Detailed wireless architecture and configuration:
- [Wireless Design Documentation](docs/wireless_design.md)
## Access Control Lists (ACL)

Access Control Lists (ACLs) are implemented to restrict management access,
isolate guest users, and control traffic flow between internal networks,
the DMZ, and the Internet.

📄 Detailed ACL policies and verification:
- [Security & Access Control Documentation](docs/security_verification.md)

## High Availability & Layer 2 Redundancy

High availability is implemented at the distribution layer using first-hop
redundancy and loop prevention mechanisms to ensure network stability and
resilience.

- HSRP is used to provide gateway redundancy for all VLANs
- EtherChannel (LACP) is deployed to increase bandwidth and link redundancy
- Spanning Tree Protocol (RSTP) prevents Layer 2 loops while maintaining
  fast convergence

📄 Detailed configuration and verification:
- [High Availability & Redundancy Documentation](docs/high_availability.md)

## Routing & Internet Connectivity

Dynamic routing and Internet connectivity are implemented to ensure full
reachability between internal networks, the DMZ, and external networks.

- OSPF is used as the interior gateway protocol across Core, Distribution, and DMZ
- NAT is configured at the network edge to provide Internet access for internal users
- Traffic flow is verified using routing tables and NAT translation entries

📄 Detailed routing and NAT verification:
- [Routing & NAT Documentation](docs/routing_nat_verification.md)

