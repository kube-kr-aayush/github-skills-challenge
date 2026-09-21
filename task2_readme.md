## Operational Data Analysis

The data contains observations from the payment-service recorded at one-minute intervals.

### Metrics
- `response_time_ms` - Response time in milliseconds
- `cpu_percent` - CPU usage
- `memory_percent` - Memory usage

### Log Information
- `log_level` - Log severity (`INFO` / `ERROR`)
- `message` - Description of the event

The `timestamp` field shows when each observation was recorded.

### Observations
Most records show normal behaviour with low response time and moderate CPU/memory usage.

The unusual observations are at time 10:05 and 10:06:
- 10:05: Response time increased to 610 ms and a payment service timeout was logged.
- 10:06: Response time increased to 640 ms, CPU reached 94%, memory reached 91%, and a database connection timeout was logged.

The values return to normal from 10:07 onwards.