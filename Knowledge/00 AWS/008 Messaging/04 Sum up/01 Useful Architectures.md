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
* SQS allows for: **data persistence**, delayed processing and retries of work