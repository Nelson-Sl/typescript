# Definition
---

An Elastic Load Balancer in Layer 7 (HTTP), Which Supports:
* HTTP / HTTP2 / WebSocket
* Load balancing to multiple HTTP applications across machines (can route to **multiple** target groups and health check is in this level)
	* **EC2 instances** (can be managed by an Auto Scaling Group) – HTTP
	* **ECS tasks** (managed by ECS itself) – HTTP
	* **Lambda functions** – HTTP request is translated into a JSON event
	* **IP Addresses** – must be private IPs
* Load balancing to **multiple applications** on the same machine (ex: containers)

Hostname: **XXX.{{region}}.elb.amazonaws.com**

# Features
---

## Routing
---
Supports Routing like:
* Routing based on **hostname** in URL (one.example.com & other.example.com)
* Routing based on **path** in URL (example.com/users & example.com/posts)
* Routing based on **Query String, Headers** (example.com/users?id=123&order=false)

![[Pasted image 20230711231004.png]]

![[Pasted image 20230711231304.png]]

## Redirect
---

Supports Redirect **between HTTP/HTTPS** and the redirect to a **dynamic port in ECS**
(Use its port mapping feature)

## IP Invisibility
---

Application Load Balancer will hide the client IP, Port and Protocol so that **application can't see the IP of client directly**. Instead they are attached in the following headers:
* IP -> **X-Forward-For**
* Port -> **X-Forward-Port**
* Protocol -> **X-Forward-Proto**

![[Pasted image 20230711235047.png]]

# Benefit
---

Great Fit for **micro-service** or **container-based** application (E.g. Docker & Amazon ECS)