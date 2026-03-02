# Security Features Overview

Terms:
- Network ACLs
- Security Groups
- Internet Gateway
- VPC
- Subnets



## Network ACLs vs Security Groups
- The internet gateway on the VPC that only permits traffic in or out of the VPC.

- The only technical reason to to use subnets in a VPC is to control access to the gateways.

- Public subnets have access to the internet while private subnets do not have access to the internet.

- Security Groups, allow specific traffic in, and by default, all traffic is allowed out. (stateful)

- Stateful means that it has some kind of memory that checks before letting traffic in.

- The Network ACL is stateless because it remembers nothing and  and checks every single packet that crosses its 
border, regardless of any circumstances.



## Subnet Boundary: Network ACLs
- Network ACLs are ideal to limit broad ranges of IP addressed access to or from a subnet.

- For example, if you're protecting a business application and you want to stop all public traffic from getting in, 
you should set up the network ACL to only allow private IP addresses to get through, which provides an additional 
line of defense.



## Instance Boundary: Security Group
- Instances have an additional layer of traffic security through security groups.

- These operate at the instance boundary.

- Network ACLs explicitly specify what traffic is or isn't allowed.

- Security group rules only specify what traffic is allowed, while all other traffic is blocked.