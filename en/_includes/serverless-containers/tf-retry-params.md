* `retry_attempts`: Number of invocation retries before the trigger moves a message to the dead letter queue. This is an optional parameter. The values may range from 1 to 5. The default value is 1.
* `retry_intervall`: Time to retry invoking the container if the current attempt fails. This is an optional parameter. The values may range from 10 to 60 seconds. The default value is 10 seconds.