# Overview of Amazon EventBridge Rules
---

* Support **SaaS apps as source** as well

![[Pasted image 20230819205718.png]]

# Use Cases
---

## Schedule: Cron jobs (scheduled scripts)
---

![[Pasted image 20230819205808.png]]

## Event Pattern: Event rules to react to a service doing something
---

![[Pasted image 20230819205922.png]]

## Event Bus
---

* AWS Service will use **default event bus**
* For SaaS Partners they can create **Partner Event Bus**
* User can create **Custom Event Bus** for custom apps

![[Pasted image 20230819210412.png]]

## Other Cases
---

* Trigger **Lambda functions**, **send SQS/SNS messages**…

# Features
---

## Archive Events & Replay
---

* You can **archive events (all/filter) sent to an event bus** (indefinitely or set period)
* Ability to **replay archived events**

## Schema Registry
---

* EventBridge can **analyze the events in your bus** and **infer the schema**
* allows you to **generate code for your application**, that will know in advance **how data is structured in the event bus**
* Schema **can be versioned**

# Permission: Resource-Based Policy
---

* Manage **permissions for a specific Event Bus**
	* E.g. allow/deny events from another AWS account or AWS region
* Use Case
	* Aggregate all events from your AWS Organization **in a single AWS account or AWS region**

![[Pasted image 20230819211141.png]]
