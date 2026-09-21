## Event Flow

The detected anomalies are converted into events and published by the `EventProducer` to the in-memory `EventTopic`.

The `EventConsumer` reads events from the same topic and processes the detected anomaly events.

The complete flow was verified successfully:

Operational Data → Anomaly Detection → Event Generation → Producer → Topic → Consumer → AIOps Output

The pipeline processed 10 records, detected 2 anomalies, and consumed 2 events successfully.

The workflow initially had a topic mismatch where the producer and consumer used different `EventTopic` instances. This was corrected by using the same topic for both the producer and consumer.