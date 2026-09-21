# AIOps Monitoring & Event Processing

This project is a Python-based AIOps simulation for monitoring a payment service,
detecting abnormal behaviour, and processing anomaly events.

## Task 1 – Project Setup
Explored the repository and identified the main components for data, anomaly
detection, event production, topics, and event consumption.

## Task 2 – Data Analysis
Analysed the service metrics and logs. The unusual behaviour was observed at
10:05 and 10:06, with increased response time and ERROR logs.

## Task 3 – Anomaly Detection
The detector processed all 10 records and identified 2 anomalies. The main
reasons were high response time, CPU/memory usage, and ERROR logs.

## Task 4 – Event Flow
Verified the flow:

Operational Data → Detector → Event → Producer → Topic → Consumer → AIOps Output

Both detected events successfully reached the consumer after fixing the topic
connection.

## Task 5 – Issues & Fixes
Two issues were corrected:
- Changed the log check from `WARNING` to `ERROR`.
- Connected the consumer to the same topic used by the producer.

The `service-events` topic declaration itself was left unchanged.

## Task 6 – Final Execution
The complete pipeline was executed successfully.

- Records processed: 10
- Anomalies detected: 2
- Events consumed: 2

## Task 7 – Documentation
Detailed observations and execution notes are available in the individual
`task1_readme.md` to `task6_readme.md` files.

## Limitation
The detector uses fixed thresholds. Using historical data or dynamic thresholds
could improve anomaly detection.

## Run

```bash
python src/aiops_pipeline.py