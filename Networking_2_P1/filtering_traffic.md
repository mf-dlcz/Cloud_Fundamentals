# Network ACL Rules Review
The rules within a network ACL dictate how it evaluates and processes traffic.

Rules are ordered based on their rule number, and evaluation begins with the lowest-numbered rule.

As traffic traverses the network ACL, it sequentially evaluates its rules until it finds a match.

Next, the network ACL runs the action specified in the first matching rule and ignores any subsequent 
rules.



## Default & Custom Network ACLs
### Default:
- When you create a new VPC, a default network ACL is automatically associated with it.

- By default, it allows all inbound and outbound IPv4 traffic and, if applicable, IPv6 traffic.


### Custom:
- Custom network ACL rules let you selectively allow or deny traffic based on your criteria, providing 
a higher level of security and customization for your VPC resources.


> [!NOTE]  
> Configuration best practice:  
> End every rule set with an explicit deny statement. The most secure filtering option is to only 
> allow by exception, where all other traffic is denied.



## Network ACL Best Practices
- Rules meant to deny traffic that are either misconfigured or ineffectual inadvertently promote 
overly permissive access to a VPC. 

    - Be mindful of the order of the deny rules within your network ACLs, because they are evaluated in 
    order.

- Know the limitations of applying network ACLs before configuring them. 

    - For example, there is a 
    default limit of 20 rules per list for both inbound and outbound network ACLs.

    - AWS can provide additional rules on request, but the absolute maximum is 40.

- Configure outbound rules to limit access to the required ports or port ranges.