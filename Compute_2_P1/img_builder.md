# Amazon EC2 Image Builder
Amazon EC2 Image builder simplies the creation, maintenance, validation, sharing, and deployment
of Linux or Windows images for use with Amazon EC2 and on-premises compute resources.

5 Key benefits of the image builder:
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

