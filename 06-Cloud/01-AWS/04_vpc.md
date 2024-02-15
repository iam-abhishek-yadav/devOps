
## Amazon VPC
A Virtual Private Cloud (VPC) in AWS is an isolated network that resembles traditional data center networks. When creating an Amazon VPC, three main factors need to be specified:

- **Name of the VPC**
- **Region:** Spans all Availability Zones (AZs) within the selected Region.
- **IP Range:** Determined using CIDR notation, defining the size of the network.

AWS then provisions a network and assigns IP addresses based on this information.

### Creating a Subnet
Subnets are smaller networks within a VPC, similar to VLANs in traditional networks. In AWS, subnets provide high availability and connectivity options. Public subnets connect to the internet, while private subnets do not. When creating a subnet, specify:
- VPC
- Availability Zone
- IPv4 CIDR block (subset of VPC CIDR block)

AWS resources, like EC2 instances, are launched into specific subnets.

### High Availability with VPC
To maintain redundancy and fault tolerance, create at least two subnets configured in different Availability Zones. This ensures resources remain available if one AZ fails.

### Reserved IPs
AWS reserves five IP addresses in each subnet for routing, DNS, and network management. For instance, in a /24 subnet, only 251 IP addresses can be assigned to resources. The reserved IPs are:
- Network Address: 10.0.0.0
- Reserved by AWS: 10.0.0.1
- Reserved by AWS: 10.0.0.2
- DNS Server: 10.0.0.3
- Future Use: 10.0.0.255

### Gateways
#### Internet Gateway
Acts like a modem, connecting the VPC to the internet. Highly available and scalable, it must be created and attached to the VPC for internet connectivity.

#### Virtual Private Gateway
Connects VPC to another private network. Establishes an encrypted VPN connection between the two sides.

### Route Tables
#### Main Route Table
- Created automatically with a new VPC.
- Contains rules (routes) for directing network traffic.
- Default configuration allows traffic between all subnets in the local network.
- Cannot be deleted or set as a gateway route table.
- Can be replaced with a custom subnet route table.
- Routes can be added, removed, and modified.
- Subnets can be explicitly associated, even if implicitly associated.

#### Custom Route Tables
- Used implicitly by subnets without explicit route table association.
- Allows customization of routes on a per-subnet basis.
- Each custom route table includes a local route for communication within the VPC.
- Protects the VPC by explicitly associating subnets with custom route tables.
- Subnets associated with custom route tables use them instead of the main route table.

### Network ACLs
A Network Access Control List (Network ACL) acts as a virtual firewall at the subnet level. It allows or denies specific inbound or outbound traffic. Consider it a security layer for subnets.

#### Default Network ACL
- Created automatically with a new VPC.
- Allows all traffic in and out of the subnet.
- Can be replaced with a custom network ACL for more granular control.

#### Custom Network ACL
- Allows customization of inbound and outbound traffic rules.
- Statelessness requires both inbound and outbound ports for protocols.
- Provides more control over traffic flow at the subnet level.

### Security Groups
Security Groups act as a virtual firewall for EC2 instances, controlling inbound and outbound traffic.

- Default configuration blocks all inbound traffic and allows all outbound traffic.
- Inbound rules must be explicitly created to allow desired traffic.
- Stateful nature remembers initiated connections.
- Organized into groups to control network communication between resources.

#### Security Group Inbound Rules Example
- HTTP (Port 80) and HTTPS (Port 443) allowed for a web server.
