# Types Used In Route 53
---
* **A**: Map a hostname to **IPv4**
* **AAAA**: Map a hostname to **IPv6**
* CNAME: Map a hostname to **another hostname** (should be A or AAAA addresses)
	* Can’t create a CNAME record **for the top node of a DNS namespace** ( E.g. **example.com** )
	* Extension: [[06 Alias Record|Alias]]
* NS: **Name / DNS Server** for [[04 Hosted Zones|Hosted Zone]]


# Types Not Used In Route 53
---

 * CAA / DS / MX / NAPTR / PTR / SOA / TXT / SPF / SRV