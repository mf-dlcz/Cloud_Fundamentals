# AWS Lambda
AWS Lambda is a compute service that makes it possible to run code without provisioning or managing servers.

Lambda runs your code on a high-availability compute infrastructure and performs all of the administration of 
the compute resources.

This includes server and operating system maintenance, capacity provisioning and automatic scaling, and logging.

Lambda is an ideal compute service for application scenarios that need to scale up rapidly, and scale down to 
zero when not in demand.

This includes file processing, stream processing, web applications, Internet of Things (IoT) backends, or mobile 
backends.


## Core Lambda Concepts
### Function:
- A function is a resource that you can invoke to run your code in Lambda.

- A function has code to process the events that you pass into the function or that other AWS services send to
the function.

### Event:
- An event is a JSON-formatted doc. that contains data from a Lambda function to process.

### Qualifier:
- When you invoke or view a function, you can include a qualifier to specify a version or alias.

- A version is an immutable snapshot of a function's code and configuration that has a numerical qualifier.

### Layer:
- A Lambda layer is a .zip file archive that can contain additional code or other content.

- A layer can contain libraries, a custom runtime, data, and configuration files.

- Using layers reduces the size of uploaded deployment archives and makes it faster to deploy your code.

### Destination:
- A destination is an AWS resource where Lambda can send events from a asynchronous invocation.

### Concurrency:
- Concurrency is the number of requests that your function is serving at any given time.

### Deployment Package:
- You deploy your Lambda function code using a deployment package.

- Lambda supports two types of deployment packages:
    - A .zip file archive: Contains function code and its dependencies. 

    - A container image: A container image includes the base operating system, the runtime, Lambda extensions, your 
    app code, and its dependencies.

### Execution Environment:
- Lambda invokes your function in an execution environment, which is a secure and isolated runtime environment.

### Instruction Set Architecture:
- The instruction set architecture determines the type of computer processor that Lambda uses to run the function.


## Lambda Function Concepts

### Timeout:
- Maximum amount of time in seconds that a Lambda function can run

- Default value is 3 seconds
    - Can be adjusted in increments of 1 sec. up to a maximum value of 15 min.

### Runtime:
- Provides a language-specific environment that relays invocation events, context information, and responses between
Lambda and the function.

- You can use runtime that Lambda provides, or build your own.

### Trigger:
- Is a resource or configuration that invokes a Lambda function.

### Extension:
- You can augment your functions with a Lambda extension.

### Handlers:
- Method in your function code that processes events.

- When your function is invoked, Lambda runs the handler method.