# What's NACL?
---

* NACL are like a firewall which **control traffic from and to subnets**
	* E.g. **Blocking a specific IP address** at the subnet level
* **One NACL per subnet**, new subnets are **assigned the Default NACL**

![[Pasted image 20230822131211.png]]

# Set up NACL Rules
---

* Rules have a number (1-32766), **higher precedence with a lower number** & **First rule match will drive the decision** (Recommended to **add rules by increment of 100**)
	* E.g. if you define #100 ALLOW 10.0.0.10/32 and #200 DENY 10.0.0.10/32, the IP address will be allowed **because 100 has a higher precedence over 200**
* The last rule is an asterisk (*) and **denies a request in case of no rule match**

## Default NACL
---

* Accepts **everything inbound/outbound** with the subnets it’s associated with
* Do NOT modify the Default NACL, **instead create custom NACLs**

![[Pasted image 20230822131937.png]]