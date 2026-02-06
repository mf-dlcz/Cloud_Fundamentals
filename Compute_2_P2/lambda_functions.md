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