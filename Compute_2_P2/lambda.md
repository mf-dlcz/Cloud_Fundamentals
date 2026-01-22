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
### **Function:**
- A function is a resource that you can invoke to run your code in Lambda.

- A function has code to process the events that you pass into the function or that other AWS services send to
the function.

### **Event:**
- An event is a JSON-formatted doc. that contains data from a Lambda function to process.

### **Qualifier:**
- When you invoke or view a function, you can include a qualifier to specify a version or alias.

- A version is an immutable snapshot of a function's code and configuration that has a numerical qualifier.

### **Layer:**
- A Lambda layer is a .zip file archive that can contain additional code or other content.

- A layer can contain libraries, a custom runtime, data, and configuration files.

- Using layers reduces the size of uploaded deployment archives and makes it faster to deploy your code.

### **Destination:**