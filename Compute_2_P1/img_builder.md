# Amazon EC2 Image Builder
Amazon EC2 Image builder simplies the creation, maintenance, validation, sharing, and deployment
of Linux or Windows images for use with Amazon EC2 and on-premises compute resources.

---
**5 Key Benefits of the Image Builder:**

1. Increased IT productivity. Image builder provides all its functionality without the need to
write and maintain automation code, freeing up resources and time.

2. Reduced exposure to security vulnerabilities.
    - allows you to create images with only the essential components.
    - Users are also able to apply AWS provided security settings to ensure that images meet 
    internal security criteria.

3. Ability to use AWS VM Import/Export to build, test, and distribute virtual machine and 
container images for EC2, as well as on-premise virtual machines.

4. Image Builder has built-in validation in the form of automated testing, which reduces errors.
    - policies can be used to prevent an image from being deployed if it has not been validated.

5. Image Builder makes it easy to manage revisions using version control.
    - It integrates with AWS Resource Access Manager and AWS Organizations to enable sharing of 
    automation scripts, recipes, and images across AWS accounts.


## Amazon Machine Images
An Amazon Machine Image (AMI) is a resource that provides the information required to launch an 
instance. 

This information includes the operating system, any preinstalled software, and configuration files 
required to run the instance.

An AMI can be as straightforward as just the OS, or customized with software applications and 
multiple storage volumes.

Customized AMIs provide faster and more efficient deployments without additional manual installation 
or user data scripts.

**An AMI includes the following:**
- One or more Amazon Elastic Block Store (Amazon EBS) snapshots, or for instance-store-backed AMIs, 
a template for the root volume of the instance (for example, an operating system, an application 
server, and applications).

- Launch permissions that control which Amazon Web Services (AWS) accounts can use the AMI to 
launch instances.

- A block device mapping that specifies the volumes to attach to the instance when it's launched.


## Shared & Public AMIs
One of the most convenient ways to get started with Amazon EC2 is to use a shared AMI that already 
has the OS and software components you need. 

You can then add your own additional content to the instance. 

With your finalized instance, you can create a new AMI. 

When you have an AMI built, _it can have one_ of the following visibilities:
- Private, so only you can use it

- Completely public, so anyone can use it

- Shared internally within an AWS account or AWS Organization

Because AWS cannot vouch for the integrity or security of all publicly shared AMIs, **you use a shared 
public AMI at your own risk.**

---
**Details to consider when sharing AMIs with the public**

1. **Regional Resource:**
    - AMIs are a Regional resource. When you search for a shared AMI (public or private), you must 
    search for it from the same Region from which it is shared.
    - To make an AMI available in a different Region, copy the AMI to the Region and then share it.

2. **AMIs that cannot be public:**
    - If the AMI contains **Encrypted Volumes, Snapshots of encrypted volumes, and Product Codes**
    the AMI can't be public.
    - You can share the AMI with specific AWS accounts.

3. **Sensitive Data:**
    - 

4. **Deprecation:**


5. **Billing:**
