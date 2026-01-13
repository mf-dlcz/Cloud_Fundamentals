# Understanding the AWS EC2 Anatomy
An Amazon Elastic Compute Cloud (Amazon EC2) instance is a virtual server in the cloud that uses a hypervisor 
to partition a portion of the host's physical hardware components (storage, 
networking, compute).

A hypervisor is a piece of virtualization software that allocates resources and manages physical hardware in a 
virtualized environment. The hypervisor allows multiple operating systems to run on a single physical server.

AWS has the following types of hypervisors:
- The original AWS hypervisor

- Nitro hypervisor that was launched with the AWS Nitro System


## AWS Nitro System
The majority of Amazon EC2 instances run on hardware known as the _AWS Nitro System_.

- The AWS Nitro System is built specifically to run instances in the most optimal way possible.

- The AWS Nitro System is a combination of dedicated hardware and a lightweight hypervisor for faster innovation 
and enhanced security.

- An important element of the AWS Nitro System hardware is how it uses dedicated hardware to offload I/O 
operations.

> [!NOTE]  
> In a traditional virtualized structure, the hypervisor is shared between a host computer's resources (such 
> as networking, storage and overall management) and customer instances.


## AWS Nitro System Resource Improvements
Hypervisors are the underlying technology behind virtualization, or the decoupling of hardware from software.

You can then create multiple virtual machines on a single host machine. Each virtual machine has its own 
operating system and hardware resources such as a CPU, a graphics accelerator, and storage. 

You can install software applications on a virtual machine, just like you do on a physical computer. 

In this structure, a hypervisor performs the following actions:
- It protects the physical hardware and its basic input/output system (BIOS)

- It virtualizes the CPU, storage, and networking functions

- It provides a rich set of management capabilities

With the Nitro System, these functions are separated and offloaded to dedicated hardware and software.

Doing this reduces costs and increases performance by delivering almost _all_ of the server resources to customer 
instances.

> [!NOTE]  
> By offloading all hardware, management, and security operations to Nitro Cards, the hypervisor no longer has 
> to dedicate a portion of compute resources to handle this input/output (I/O).

The Nitro System uses multiple Nitro Cards on a host, each focusing on a singular function.

The Nitro System uses the following cards: 

- Nitro Card for VPC
- Nitro Card for EBS
- Nitro Card for Instance Storage
- Nitro Card Controller
- Nitro Security Chip


## Benefits of Nitro Hypervisor
### <ins>Faster Innovation<ins>
- Modular Design: It is built as a collection of modular building blocks that can be assembled in various ways.

- Rapid Delivery: This flexibility allows AWS to quickly design and release new EC2 instance types with a wide 
range of compute, storage, memory, and networking options.

- Bare Metal Support: This innovation led to the creation of bare metal instances, which allow you to bring 
your own hypervisor or run without one entirely.


### <ins>Enhanced Security<ins>
- Continuous Monitoring: It constantly protects and verifies the integrity of the instance's hardware and 
firmware.

- Minimized Attack Surface: By offloading virtualization resources to dedicated hardware and software, it 
reduces potential vulnerabilities.

- Locked-Down Model: The system is designed to prohibit administrative access, which removes the risks of human 
error and tampering.


### <ins>Better Performance and Price<ins>
- Maximum Resource Delivery: Because it offloads management tasks, it delivers nearly all of the host's compute 
and memory resources directly to your instances.

- High-Speed Hardware: It uses dedicated Nitro Cards to provide accelerated I/O, including high-speed networking 
and EBS storage.

- Cost Efficiency: By eliminating the need to reserve resources for management software, AWS can pass those 
savings on to the customer.

### <ins>Support for Previous Generation Instances<ins>
- Longer Service Life: It allows older EC2 instance types to stay active longer than the physical hardware 
they originally ran on.

- Modern Foundation: AWS uses new Nitro hardware and software components to keep these older instances running 
smoothly.

- No Migration Needed: This means you can keep your workloads on the same instance families you've already 
built, without having to upgrade or change them.


## Network Interface