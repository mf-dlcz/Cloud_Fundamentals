# Network Gateways
A network gateway is a device that connects networks with different transmission protocols, and performs
protocol conversions to translate communications.

The network gateway has a network interface card with inputs, outputs, and software for the translation 
of network protocols.

Network gateways serve as an entry and exit point for a network.



### Internet Gateway
- Internet gateway is an Amazon VPC component that allows communication between your computer and the internet. 


### Customer Gateway
- Customer gateways are physical appliances or software that you own or manage in your on-premises network.

- Applications include the management of routing to and from your environment.


### VPN Gateway
- VPN gateway is the gateway on the AWS side of a site-to-site VPN connection.


### NAT Gateway
- NAT gateway is a network address translation service that makes it possible for instances in a private
subnet to connect to services outside of your VPC.


### AWS Direct Connect Gateway
- Direct Connect gateway establishes connectivity that spans Amazon VPCs that are spread across multiple 
Regions.


### Transit Gateway
- Transit gateways connect Amazon VPCs, AWS accounts, and on-premises networks to a single gateway.


### Virtual Gateway
- Virtual gateways make it possible for resources outside your mesh network to communicate to resources
inside the mesh network.



## Internet Getway Overview
- With internet gateways, instances in your VPC public subnet can have direct access to the internet.

For the resources in a VPC to send and receive traffic from the internet, complete the following steps:

1. Create an internet gateway and attach it to a VPC

2. Add a route to your route table to allow traffic to and from the internet gateway.

3. The security groups and network access control lists (network ACLs) associated with your VPC must 
allow traffic to and from the internet.

4. Your subnet's resources must have a public IP address or an attached Elastic IP address.



> [NOTE!]  
> When an internet gateway is attached to a subnet, it creates a public subnet by performing a type of 
> NAT called static NAT. The internet gateway will allocate a resource with a public IPv4 IP address. 
> When packets pass through the internet gateway, the internet gateway switches the source IP address 
> from the private IP address to the public one. Next, it sends the packet on. When the packet returns, 
> it switches the destination address from the public IP address back to the private IP address.