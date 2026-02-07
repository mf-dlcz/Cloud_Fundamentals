# Optimizing a Lambda Functions
- How to mesure performance in an app.

**End To End**
- Use a tool similar to Locust which measures 
    - average response time
    - maximum response time
    - 90th percentiles
    - failure rate
    - requests per sec

_End-to-end_ metrics include network latency and other AWS service durations, not just Lambda duration time.


---
**Lambda**
- The Lambda console provides metrics that focus specifically on your Lambda function's internal performance.

- These metrics can help you understand if performance issues are in your Lambda code or in other user request components.

- Lambda metrics include:
    - duration: time code spends processing
    - invocations: number of times function was called
    - concurrent invocations: how many instances run simultaneously
    - error count: function-level failures
    - throttles: requests rejected due to concurrency limits


## Memory Optimization
- Memory is the principle lever for controlling the performance of a function.

- Lambda allocates CPU power in proportion to the amount of memory configured for a function.

- The **memory** setting allows you to increase or decrease the memory and CPU power allocated to your function.

- To find the right memory setting, you can monitor your functions with Amazon CloudWatch and set alarms if memory consumption
is approaching the configured maximums.


## Provisioned Concurrency
- Increasing a Lambda function setting called _provisioned concurrency_ can help reduce the function's max response time.

**Cold starts can affect app performance**


## Cold starts & the Lambda lifecycle
When the Lambda service receives a request to run a function through the Lambda API, the following four main actions happen.

1. Download you code:  
The Lambda service downloads your code from an S3 bucket or a container registry depending on the packaging of your function.

2. Start new execution environment:  
Lambda creates an environment with the memory, runtime, and configuration that you have specified.

3. Run initialization code:  
Lambda then runs any initialization code outside the event handler.

4. Run handler code:  
Lastly, Lambda runs the event handler code for your function.


> [!NOTE]  
> The first two steps in the process are frequently referred to as a _cold start_.  
> You're not charged for the time it takes for Lambda to prepare the function, but it does _add latency_ to the overall 
> invocation duration.  
> After the function execution completes, the execution environment is frozen. To improve resource management and performance, 
> the Lambda service retains the execution environment for a nondeterministic period of time. During this time, if another 
> request arrives for the same function, the service may reuse the environment. This second request typically finishes more 
> quickly, since the execution environment already exists, and it’s not necessary to download the code and run the 
> initialization code. This is called a warm start.


## Minimizing Cold Start Latency
