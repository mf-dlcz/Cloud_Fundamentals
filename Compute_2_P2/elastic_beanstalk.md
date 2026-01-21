# Understanding AWS Elastic Beanstalk
With AWS Elastic Beanstalk, you can upload your application, and it automatically handles the 
deployment details of **capacity provisioning, load balancing, auto-scaling, and application 
health monitoring.** 

By using Elastic Beanstalk, you can focus on developing your application instead of the following 
deployment-oriented tasks:

- Provisioning servers

- Setting up load balancing

- Managing scaling


## Elastic Beanstalk Concepts:

1. **Application:**
    - An Elastic Beanstalk application is a logical collection of Elastic Beanstalk components, 
    including environments, versions, and environment configurations. 
    
    - In Elastic Beanstalk, an application is conceptually similar to a folder.


2. **Application Version:**
    - An application version refers to a specific, labeled iteration of deployable code for a web 
    application.

    - An application version points to an Amazon S3 object that contains the deployable code, such as 
    a Java WAR file.

    -  Applications can have many versions, and each application version is unique.

    - You might upload multiple application versions to test differences between one version of your 
    web application and another. 


3. **Environment:**
    - An environment is a collection of AWS resources running an application version.

    - Each environment runs only one application version at a time.

    - However, you can run the same application version or different application versions in many 
    environments simultaneously.


4. **Environment Tier:**
    - When you launch an Elastic Beanstalk environment, you first choose an environment tier. 
    
    - The environment tier designates the type of application that the environment runs, and determines 
    what resources Elastic Beanstalk provisions to support it. 
    
    - An application that serves HTTP requests runs in a web server environment tier.
    
    - A backend environment that pulls tasks from an Amazon Simple Queue Service (Amazon SQS) queue 
    runs in a worker environment tier.


5. **Environment Config:**
    - An environment configuration identifies a collection of parameters and settings that define 
    how an environment and its associated resources behave. 
    
    - When you update an environment’s configuration settings, Elastic Beanstalk automatically 
    applies the changes to existing resources or deletes and deploys new resources (depending on the 
    type of change).


6. **Saved Config:**
    - A saved configuration is a template that you can use as a starting point for creating unique 
    environment configurations. 
    
    - You can create and modify saved configurations, and apply them to environments, using the 
    Elastic Beanstalk console, Elastic Beanstalk Command Line Interface (EB CLI), AWS Command Line 
    Interface (AWS CLI), or API.
    
    - The API and the AWS CLI refer to saved configurations as configuration templates.


7. **Platform:**
    - A platform is a combination of an operating system, programming language runtime, web server, 
    application server, and Elastic Beanstalk components. 
    
    - You design and target your web application to a platform. Elastic Beanstalk provides a variety 
    of platforms on which you can build your applications.


## Steps for using Elastic Beanstalk
1. Create a web app

2. Create an AWS Elastic Beanstalk app

3. Create an environment for the app

4. Upload a zip of your app

5. Deploy your app to running resources or select an older version

6. Save the environment


> [!NOTE]  
> When you deploy your application, AWS Elastic Beanstalk deploys web server applications or worker applications.