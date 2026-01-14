# Understanding the EC2 Lifecycle
The amazon EC2 instances has a few states
- pending
- running
- shutting-down
- terminated
- stopping
- stopped

### <ins>Pending<ins>
- The instance is preparing to enter the running state.
- An instance enters the pending state when it is launched or when it is started after being in the 
stopped state.
- This phase is _not_ billed.

### <ins>Running<ins>
- The instance is running and ready for use.
- You are billed while an instance is in the running state.
- The instance remains in the running state during a reboot. 

### <ins>Shutting Down<ins>
-The instance is preparing to be terminated.
- This phase is not billed.

### <ins>Terminated<ins>
- When you decide that you no longer need an instance, you can terminate it.
- In the terminated state, the instance has been permanently deleted and cannot be started anymore.

### <ins>Stopping<ins>
- The instance is preparing to be stopped.
- This phase is not billed.

### <ins>Stopped<ins>
- The instance is shut down and cannot be used.
- The instance can be started at any time.