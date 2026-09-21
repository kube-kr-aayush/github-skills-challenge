## Anomaly Detection
changed the wronng code from if record["log_level"] == "WARNING": to 
The detector processed all 10 records and identified 2 anomalies at 10:05 and 10:06.

The anomalies were detected due to high response time, and the 10:06 record also had high CPU and memory usage. Both records contained ERROR logs, which were also identified by the detector.

No obvious normal record was flagged.