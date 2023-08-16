# SQS + SNS: Fan Out
---

* Push once in SNS, **receive in all SQS queues that are subscribers**
* Make sure your **SQS queue access policy allows for SNS to write**

![[Pasted image 20230816214835.png]]

## Advantage
---

* **Fully decoupled, no data loss**
* Scalability: **Ability to add more SQS subscribers over time**
* Cross-Region Delivery: **works with SQS Queues in other regions**
* SQS allows for: **data persistence**, **delayed processing** and **retries of work**

# SNS FIFO + SQS FIFO: Fan Out
---
* Fan out + Ordering + Deduplication

![[Pasted image 20230816215207.png]]

# SNS + Kinesis Firehose + S3
---

![[Pasted image 20230816215352.png]]
