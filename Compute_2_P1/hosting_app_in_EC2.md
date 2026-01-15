# Hosting an App on Amazon EC2

- Hosting a static website using Amazon S3
    - Pros: Cost effective, serverless, no scaling
    - Cons: S3 endpoints do not support HTTPS

- Hosting an app in containers using Amazon EC2
    - Pros: Supports dynamic websites
    - Cons: Operational efforts including building, versioning, and deploying containers
        - Scaling considerations

- Using Amazon Elastic Beanstalk
    - Pros: Supports dynamic websites
        - Infrastructure including load balancing and autoscaling managed by AWS
        - Reduced operational complexity
    - Cons: Less control for custom app architectures

- Using AWS Lambda
    - Pros: Serverless
        - Best option for event-driven, short-duration tasks
        - Automatically scales
    - Cons: Only suitable for distributed apps or responses to events
        - Limited duration

- Using Amazon EC2
    - Pros: Full control of configuration
        - Most similar to on-premises deployment
    
    - Cons: Operational effort including managing AMIs, scaling, availability and deployment