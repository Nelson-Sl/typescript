# What is EC2 Instance Store?
---

An instance store provides a **temporary block-level storage / hardware disk**  to your instance (Physical storage attached to instance host). It provides **better I/O performance** than EBS.

Note: EC2 Instance Store has the risk of **lost all data** if instance has been stopped or the hardware has failed. Therefore remember to **backup or replicate**

# Use Cases
---

Store for **Temporary Data** (E.g. cache, stratch data, buffer)