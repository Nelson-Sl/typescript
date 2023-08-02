# How the storage auto scaled?
---

RDS will automatically scale the storage till reach the **maximum storage threshold** if:
* Free storage is **less than 10%** of its allocated storage
* Low storage has been lasted for **at least 5 minutes**
* The last modification **has been passed for 6 hours**
![[storage_auto_scaling.png]]

# Support
---

It supports **all relational database engine** (MySQL, Oracle, MariaDB, PostgreSQL, Microsoft SQL Server)

# Benefit
---

Fits for **unpredictable workload**