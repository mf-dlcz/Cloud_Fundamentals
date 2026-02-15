# VPC Fundamentals Review

- subnets
- internet gateways
- route tables
- elastic IP adresses
- elastic network interface
- NAT gateways


## Amazon VPC
- A VPC is your network environment in the cloud

- With Amazon VPC, you launch AWS resources into a virtual network that you have defined

- VPCs deploy into one of the AWS Regions, and can host resources from any Availability Zones within its Region


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

- An internet gateway performs NAT by mapping a public and private IP address


## Route Tables
- A route table contains a set of rules called **routes** that the VPC uses to determine where to direct network
traffic.

- When you create a VPC, it automatically has a main route table.

- Initially the main route table and every other route table in the VPC contains _only_ one single route.

- It's a local route that permits communication to all the resources within a VPC.

- You can create additional custom route tables for your VPC.

- Each subnet in your VPC must be associated with a route table.

- If you don't explicitly associate a subnet with a particular route table, the subnet is implicitly associated
with, and uses the main route table.


## Private Subnets
- Allow indirect access to the internet.

- Traffic stays within your private network.

- A private IP address assigned to an EC2 instance will never change, unless you manually assign a new IP address on
the network interface of the EC2 instance.


## Elastic IP Addresses
- Is a static public IPv4 address designed for dynamic cloud computing.

- You can associate an Elastic IP address with any instance or network interface for any VPC in your account.

- With an Elastic IP address, you can mask the failure of an instance by rapidly re-mapping the address to another
instance in your VPC.

- You can move an Elastic IP address from one instance to another.

- The instance can be in the same VPC or another VPC.

- An Elastic IP address is accessed through the internet gateway of a VPC.


## Elastic Network Interfaces
- An Elastic Network Interface is a logical networking component in a VPC that represents a virtual network card.

- When moved to a new intances, the network interface maintains its public and Elastic IP address, its private and
Elastic IP address, and MAC address.

- The attributes of a network follow it.


## NAT Gateways
- NAT is used for IP address conservation

- Because NAT maps private IP addresses to a public address, you can use it to allow private IP networks to connect
to the internet.


## VPC Security Features
