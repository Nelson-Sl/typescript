* Figure out **caching solution** if there's some question about database cost saving, instead of read replicas
* Make sure to **setup one more instance / AZs** when related to availability questions
* Think Route 53 for health check when related to infrastructure
	* Route 53 DNS Failover handles all of these failure scenarios by integrating with ELB behind the scenes. Once enabled, Route 53 automatically configures and manages health checks for individual ELB nodes.
* S3 
	* Website
		* s3-website dash (-) Region ‐ http://bucket-name.s3-website.Region.amazonaws.com
		* s3-website dot (.) Region ‐ http://bucket-name.s3-website-Region.amazonaws.com
	* Event Notification only support SQS Standard but not SQS FIFO
* DataSync & File Gateway
	* Migrating Existing Data -> DataSync
	* Ongoing Migration of Existing data & Patch Updates -> File Gateway