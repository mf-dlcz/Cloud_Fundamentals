# VPC Fundamentals Review
- Amazon VPC
- subnets
- internet gateways
- route tables
- elastic IP adresses
- elastic network interface
- NAT gateways


## Amazon VPC
- A VPC is your network environment in the cloud

- With Amazon VPC, you launch AWS resources into a virtual network that you have defined

- VPCs deploy into one of the AWS Regions, and can host resources from any Availability Zones within 
its Region


## Subnets
- A subnet is a range of IP addresses in your VPC

- You can launch AWS resources into a specified subnet

- Use a public subnet for resources that must be connected to the internet, and a private subnet for 
the resources that won't be directly connected to the internet.

- A subnet resides within one Availability Zone.

- Your public subnet configuration acts as a two-way door. It allows traffic to flow in either direction:
invited or not invited. Since there is no automatic outbound routing, you must configure a subnet to be public.
A public subnet requires the following: an _internet gateway_ that allows communication between resources in your
VPC and the internet, a _route table_, which contains a set of rules called routes that are used to determine where
network traffic is directed, a _public subnet_ has a route table with a direct route to the internet gateway, and
_public IP addresses_, which are addresses that are accessible from the internet. 


## Internet Gateways
- Is a VPC component that permits communication between instances in your VPC and the internet.

- An internet gateway serves two purposes
    - It provides a target in your route table for internet routable traffic
    - It protects IP addresses on your network by performing network address translation or NAT.