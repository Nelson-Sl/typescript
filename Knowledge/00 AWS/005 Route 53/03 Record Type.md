# Types Used In Route 53
---
* **A**: Map a hostname to **IPv4**
* **AAAA**: Map a hostname to **IPv6**
* CNAME: Map a hostname to **another hostname** (should be A or AAAA addresses)
	* Can’t create a CNAME record **for the top node of a DNS namespace** ( E.g. **example.com** )
* NS: **Name / DNS Server** for Hosted Zone, which control the way traffic is routed to domain


# Types Not Used In Route 53
---

 * CAA / DS / MX / NAPTR / PTR / SOA / TXT / SPF / SRV