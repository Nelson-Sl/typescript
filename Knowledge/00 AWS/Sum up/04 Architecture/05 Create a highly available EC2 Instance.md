# Case 1: Standby Instance
---

*  **Create a standby EC2 Instance in another AZ** so it could keep available when the system failed

![[Pasted image 20230824090150.png]]

# Case 2: Instances with ASG
---

![[Pasted image 20230824090256.png]]

# Case 3: Instance with ASG + EBS
---

* **Create EBS Snapshot** & **Restore at the new EC2 Instance** in new AZ

![[Pasted image 20230824090506.png]]
