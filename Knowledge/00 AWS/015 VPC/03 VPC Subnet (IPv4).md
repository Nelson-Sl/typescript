# Features
---

* AWS reserves **5 IP addresses** (first 4 & last 1) in each subnet, which are **not available for use** and **can’t be assigned to an EC2 instance**

## Examples
---

If CIDR block **10.0.0.0/24**, then reserved IP addresses are:
* 10.0.0.0 – **Network Address**
* 10.0.0.1 – reserved by AWS for the **VPC router**
* 10.0.0.2 – reserved by AWS for **mapping to Amazon-provided DNS**
* 