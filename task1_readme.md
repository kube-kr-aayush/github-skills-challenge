

This project simulates monitoring of a payment application service using operational
metrics and logs. The service produces infoprmation such as response time, CPU usage,
memory usage, log level, and log messages.

## operational problem being addressed 

The objective is to identify unusual behaviour in the payment service. Abnormal response times, high resource utilization, and concerning log events can indicate operational issues that should be detected and processed as anomaly events.

## Purpose of AIOps

The AIOps workflow analyses operational data, detects abnormal behaviour, generates
anomaly events, and processes those events through a lightweight simulated event
pipeline.

The workflow is:

Operational Data → Anomaly Detection → Event Generation → Producer → Topic → Consumer → AIOps Output
