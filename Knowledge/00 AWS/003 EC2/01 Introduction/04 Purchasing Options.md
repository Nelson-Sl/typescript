# Options

## EC2 On Demand
---

* Payment Schedule
	* Billing fix rate for Linux & Windows **per second**, after first minute
	* Billing fix rate for other systems **per hour**
* Characteristics
	* No **upfront payment** (预付款)
	* No **long-term commitment** (长期投入)

## EC2 Capacity Reservations
---

* Payment Schedule
	* Reserve On-Demand instances capacity **in a specific AZ** at any duration
	* Charge on On-Demand rate whenever you are running instances or not
* Characteristics
	* Can access to it whenever you need it
	* No time commitment but **no billing discounts** (Should combine with Reserved Instances or Saving Plans to get discount)

## EC2 Reserved Instances
---

* Payment Schedule
	* Reserve a specific instance attributes (Instance Type, OS, Region, Tenancy, etc.) for **1-3 years**. The longer the reservation period, **the higher discount**.
	* The scope of Instance's scope could be **Regional** or **Zonal**.
	* Payment Options
		* **No Upfront** Payment (Less Discount)
		* **Partial Upfront** Payment (Medium Discount)
		* **Full Upfront** Payment (Highest Discount)
* Characteristics
	* Up to **72%** discounts compared to On Demand
	* Can **buy or sell** in Reserved Instance Market Place

## EC2 Convertible Reserved Instances
---

*  Same as EC2 Reserved Instances Except
	* Can convert **instance attributes** (E.g. Instance Type, Instance Family, OS, Region, Tenancy and Scope, etc.)
	* Up to **66%** discount compared to On Demand

## EC2 Saving Plan
---

* Payment Schedule
	* Get a discount (up to **72%**) for a long-term usage
		* E.g. $10/hour for 1-3 year usage
	* Will come to On Demand if beyond saving plan
* Charateristics
	* Lock Into a specific **instance family** and **region** (E.g. M5 us-east-1), and flexible across **instance size** (E.g. m5xlarge), **OS** (Linux / Windows) and **Tenancy** (Dedicated / Host / Default)

## EC2 Spot Instance
---

* Payment Schedule
	* Instance will lost at the point of time when your **max price is less than current spot price** (stop or terminate in a 2-minute grace period)
	* Spot Block (Deprecated): "block" spot instance during a specific time frame (1-6 hours without interruptions). In **rare situations**, the instance can be **reclaimed**.
* Characteristics
	* Up to **90%** discount Compared to On-Demand (Most Efficient)
* Cancelling & Terminate Spot Instances
	* A spot instance can only be cancelled when it is **open**, **active** or **disabled**
	* Firstly Create a **cancel spot instance request**, then **terminate the associated instances**
* Optional Strategy: [[04 Purchasing Options#Spot Fleets|Spot Fleets]]


## EC2 Dedicated Hosts
---
* Definition
	* A physical with EC2 Instance **capacity** **fully dedicated to your use**, which allows you address **compliance requirements** and use your existing **server-bound software licenses** (per socket, per core, per VM e.g. Linux Enterprise Server)
* Payment Option
	* On-demand: pay **per second** for each dedicated host
	* Reserved: **1 or 3 years** (No Upfront - Partial Upfront - All Upfront)
* Characteristics
	* Most Expensive Options

## EC2 Dedicated Instances
---
* Definition
	* A physical with EC2 Instance **fully dedicated to your use**, might share hardware with other instances in the same account
* Payment Option
	* Same as Dedicated Hosts but billing based on instance
* Difference with Dedicated Hosts
	* No **host visibility** (E.g. socket, cores, host ID)
	* No **control over instance placement** (move hardware after instance start/stop)
![[ec2_dedicated_instance.png]]

## Spot Fleets
---

* Definition: set of **Spot Instances** + (Optional) **On-Demand Instances**, it can automatically choose the spot instance with **lowest price** from **launching pools** with different AZ, OS and instance types (E.g. m5 large).
* Payment Strategies
	* **LowestPrice**: Choose the instance from the pool with lowest price (Suits for **short-term**, **cost-optimization** workload)
	* **Diversified**: Choose instances from all available launching pools (Suits for long-term workload with requirements on availability)
	* **capacityOptimized**: Choose instance from the pool with optimal capacity
	* **priceCapacityOptimized** (**Recommended**): Choose launching pools with optimal capacity first, then choose instances with lowest prices (Suits for most workloads)
* Characteristics: It will stop raising instances when reaching **max capacity or cost**

# Recommendation to choose pricing solution
---

* Short-term & Uninterrupted Workloads (Can't predict how application behave): **On Demand**
	* Specified in AZ: **Capacity Reservations**
* Long-term & Steady-Stage Usage Applications (E.g. think database): **Reserved / Convertible Reserved Instances**
	* For Lower long-term running cost: **Savings plan**
* **Workload that are resilient to failure** (E.g. Workload with flexible start & end time, distributed workloads like batch jobs, data analysis, image processing): **Spot Instances**
* Companies that **have strong regulatory and compliance needs**, or need to use software that have **complicated licensing model** like Bring Your Own License (BYOL): Dedicated Hosts/Instances

# Pricing Reference
---

![[ec2_price_options.png]]
