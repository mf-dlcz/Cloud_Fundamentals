# EC2 Networking Overview
- You use Amazon EC2 to create and run virtual machines called EC2 instances.

- You have the flexibility to choose from a wider range of instance types tailored for different workloads and
performance requirements.



## EC2 Instance Launch Considerations

### Tags
- Tags allow you to manage resources access control, track costs, help automate tasks, and stay organized.


### Application & OS imgs
- Amazon Machine Imgs (AMIs) provide the software information required to launch an instance (EX. operating system,
application server and apps).


### Key Pairs
- A key pairs consists of a private and public keys for security credentials.

- The key pair is used to prove your identity when connecting to an instance.


### Scripts & metadata
- Scripts enable automation of tasks such as software installation and configuration

- Metadata provides essential information about the instance, such as instance ID and public IP address, facilitating
resources management, and app development.


### Storage
- Each storage option has a unique combination of performance and durability.



## Location when launching an EC2 Instance

### Regions
- Regions represent a geographic area, and they are designed to provide low-latency connectivity to the services
and resources in them.


### Availability Zones
- Designed to be independent of each other, with separate power, cooling, and networking infrastructure to ensure
fault tolerance.

- By distributing instances across availability zones, you protect your application from failures that might occur
in a single availability zone.


### Local Zones
- Local zones are an extension of AWS Regions, and are geographically located in proximity to metropolitan areas.

- Local zones could be used to deploy apps closer to end users in metropolitan areas, reducing latency for specific
workloads.

- Local zones must be enabled before use



## Instance Communication Basics

### Dynamic Host Configuration Protocol (DHCP)
- DHCPis a networking protocol you use to automatically assign IP addresses and network configuration information
to devices in a network.

- DHCP automatically assigns private IP addresses to EC2 instances that you launch in a VPC.


### DNS
- DNS is a protocol you use to translate domain names into IP addresses.



## Hostnames
When you launch an EC2 instance, it is assigned a private DNS hostname and a public DNS hostname

- The private DNS hostname is used for communication in your VPC

- The public DNS hostname is used for accessing the instance from the internet



## Network Interface Types

### Elastic Network Interface
- An elastic network interface is a logical networking component in a VPC that represents a virtual network card.

- It provides networking capabilities, such as assigning private IP addresses, attaching security groups, and 
configuring network settings


### Elastic Network Adapters (ENAs)
- ENAs are custom network interfaces that deliver enhanced networking performance for EC2 instances.


### Elastic Fabric Adapters (EFAs)
- EFAs are network adapters that provide low-latency, high bandwidth, and secure communication for EC2 instances 
in high performance computing (HPC) and machine learning (ML) scenarios. 

- You typically use EFAs in parallel computing, simulation, and data analysis applications