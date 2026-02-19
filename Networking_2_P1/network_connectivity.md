# Public IP Addresses Overview
EC2 instances in AWS are assigned two IP addresses at launch: a private address and a public address. 

The private address is used for communication between instances in the same VPC, and the public address is used 
for communication over the internet.

> [NOTE!]  
> A public IP address associated with an instance can change whenever the instance is restarted.


### Default VPC
- A default VPC is suitable for getting started quickly, and for creating simple applications.


### Non-Default VPC
- When you launch an instance into a non-default VPC, it checks an attribute in the subnet.

- The attribute determines whether instances launched into that subnet can receive a public IP address from 
the public IPv4 address pool.

- By default, instances launched in a non-default subnet are not assigned a public IP address.



## Public IP address Pool Assignments
All of the public IP addresses are assigned from a pool of public IPv4 addresses at Amazon.

When a public IP address is disassociated from your instance, it is released back into the public IPv4 address 
pool, and you cannot reuse it.

### Public IP Address Released
- When your instance is stopped, hibernated, or terminated, your IP address is released. Your stopped or 
hibernated instance receives a new public IP address when it is restarted. 

- Your IP address is released when you associate an Elastic IP address with it. When you disassociate the 
Elastic IP address from your instance, it receives a new public IP address.


### Public IP Address Saved
- If there is more than one elastic network interface attached to your instance.

- If your instance's public IP address is released while it has a secondary private IP address that is 
associated with an Elastic IP address.



## Elastic IP Addresses
- An Elastic IP address is a static public IPv4 address associated with your AWS account in a specific Region. 

- **Unlike an automatically assigned public IP address, an Elastic IP address is preserved after you stop and 
start your instance in a VPC.**

- You can't retain or reserve the current public IP address assigned to the instance using an automatically 
assigned public IP address.

- You cannot convert an automatically assigned public IP address to an Elastic IP address.

- There is a default limit of five Elastic IP addresses per Region for each AWS account. 

- You are charged a small fee for any Elastic IP address that is not associated to a running instance.

> [!NOTE]  
> An Elastic IP address remains associated with your AWS account until you release it, and you can move it from 
> one instance to another as needed. You can bring your own IP address range to your AWS account. It appears as 
> an address pool, and you can allocate Elastic IP addresses from your address pool.



## Elastic Network Interface Overview
An elastic network interface is a logical networking component that represents a virtual network card.

The network interface makes it possible for the host instance to communicate on the network to other hosts, 
resources, and the external internet.

When you create a security group, the security group is associated with the network interface. Traffic that 
attempts to connect to the network interface must have a security group rule that allows inbound access to the 
instance.

### Primary Network Interface
- Is created by default when the instance is created.

- You cannot detach or move a primary network interface from the instance on which it was created.


### Secondary Network Interface
- Is an additional interface you create and attach to the instance.

- The maximum number of network interfaces you can use varies by instance type.