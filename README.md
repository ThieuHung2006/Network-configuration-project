# Network Configuration Project

This project simulates an enterprise network topology based on a 3-layer
architecture (Core, Distribution, and Access). The design demonstrates
routing, segmentation, security, high availability, and enterprise services
in a realistic corporate environment.

## Network Devices Configured
- **Core Routers**: Core_1, Core_2
- **DMZ Router**: Router_DMZ
- **ISP Router**: ISP

## Project Features
- **OSPF** for dynamic and scalable routing
- **VLANs & Inter-VLAN Routing** for network segmentation
- **DHCP & DNS Services** deployed in the DMZ
- **Security Controls** using ACLs and NAT
- **High Availability** with HSRP, STP, and EtherChannel
- **Enterprise Wireless** using WLC with WPA2-Enterprise and Guest access

## Folder Structure
- `configs/`: Device configuration files (routers & switches)
- `docs/`: Design and verification documentation
- `images/`: Network topology diagrams and verification screenshots

## How to Use
1. Clone the repository.
2. Load the configuration files onto the corresponding network devices.
3. Verify connectivity, routing, security policies, and services.

## Network Topology

The diagrams below illustrate the complete enterprise network design using a
3-tier architecture, including DMZ and ISP connectivity.

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

## Infrastructure Services

Core enterprise services are deployed in the DMZ to support network operations.

- DHCP for dynamic IP assignment
- DNS for internal name resolution
- AAA (RADIUS) for secure wireless authentication
- Web services published via static NAT

📄 Detailed service verification:
- [Infrastructure Services Documentation](docs/infrastructure_services_verification.md)
