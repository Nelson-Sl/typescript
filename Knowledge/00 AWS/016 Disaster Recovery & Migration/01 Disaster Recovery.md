# What's Disaster Recovery?
---

* Disaster recovery (DR) is about preparing for and recovering from a **disaster**, or any event that **has a negative impact on a company’s business continuity or finances**
	* On-premise => On-premise: **traditional DR, and very expensive**
	* On-premise => AWS Cloud: **hybrid recovery**
	* AWS Cloud Region A => AWS Cloud Region B

# Disaster Recovery Strategy
---

## Evaluation Term
---

* Recovery point objective (RPO)
	* the maximum amount of data – as measured by time – **that can be lost after a recovery from a disaster, failure, or comparable event** before data loss will exceed what is acceptable to an organization.
* Recovery time objective (RTO)
	* The **duration of time and a service level** within which a **business process must be restored after a disaster in order to avoid unacceptable consequences associated with a break in continuity.**

![[Pasted image 20230823170700.png]]

## Backup & Restore 
---

* High **RPO** & **Slower RTO**

![[Pasted image 20230823170828.png]]

## Pilot Light
---

* Very similar to Backup and Restore but a small version of the app is always running in the cloud
