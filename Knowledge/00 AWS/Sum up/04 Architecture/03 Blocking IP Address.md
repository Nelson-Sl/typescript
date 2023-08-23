# Origin Case
---

* **NACL** + **Optional Firewall Software in EC2**

![[Pasted image 20230823215425.png]]

# With an ALB
---

* **NACL** + **ALB Connection Termination**

![[Pasted image 20230823215510.png]]

## ALB + WAF
---

* WAF for **IP address filtering**

![[Pasted image 20230823215624.png]]

## ALB, CloudFront + WAF
---

* WAF for **IP address filtering**, Cloudfront for **Geo Restriction**
* NACL Not helpful in this case since 

![[Pasted image 20230823215815.png]]