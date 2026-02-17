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

- Unlike an automatically assigned public IP address, an Elastic IP address is preserved after you stop and 
start your instance in a VPC.

