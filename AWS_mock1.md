 It is unknown how often the logs will be accessed or which logs will be accessed the most : use **s3 intelligent tiering**

 key_value + Initially, the data requirements will be around 1 GB and future growth is unknown. Requests can range from 0 to over 800 requests per second :**dynamo db and lambda**

 highest availability and low operational complexity : **multi az and ASG**

 the middle tier uses EC2 instances and an Amazon SQS queue to process orders : to process it fastly use **Use Amazon EC2 AutoScaling** to scale out the middle tier instances based on the SQS queue depth.

 A company is working with a strategic partner that has an application that must be able to send messages to one of the company’s Amazon SQS queues. The partner company has its own AWS account: grant the **sqs:SendMessage permission** to the partner’s AWS account.
 
 send data in near-real time: **Kinesis data streams or firehouse**

 highly available multiplayer game on AWS + layer4 : Configure an Auto Scaling group to add or remove instances in **multiple Availability Zones** automatically **and NLB**(cost effective coz using ASG)

 AWS IAM user accounts have specific complexity requirements and minimum password length: **Set a password policy for the entire AWS account.**

 Distribution rights for the content require that users in different geographies must be served content from specific regions.: **Create Amazon Route 53 records with a geolocation routing policy.**

 you **can't Enable encryption in transit** using the **RDS Management console** and obtain a key using AWS KMS. Instead u can use **AWS ROOT CERTIFICATES**

 BACKUP website : use **static website on S3** and create **ROUTE53 failover routing policy**

**ECS TASKS**: Create an IAM policy with permissions to DynamoDB and assign It to a task using the **taskRoleArn parameter**

Distributed File System Replication**DFSR**: amazon **FSX**

Create an SCP with a **deny rule** that denies all but the specific instance types: DENY RULE IS MORE POWERFUL THAN ALLOW RULE

Use a **separate SQS Standard queue** for each tier. Configure Amazon EC2 instances to **prioritize polling for the paid queue** over the free queue.

Create a **Nitro-based Amazon EC2 instance** with an Amazon EBS Provisioned IOPS SSD (i01) volume attached. Provision 64,000 IOPS for the volume.

cost-effective : PRICE CLASS

A team are planning to run analytics jobs on log files each day and require a storage solution. The size and number of logs is unknown and data will persist for 24 hours only: **USE S3 STANDARD** (DON'T use intelligent tiering coz it will cost u)

Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages.

You **can't deploy RDS MULTI AZ in another region**. AZ is different and region is different

2 ip address : GLOBAL ACCELERATOR

Microsoft SQL Server database to AMAZON RDS : Use the **AWS Database Migration Service (DMS)** to directly migrate the database to RDS

3,000 IOPS: Amazon EBS General Purpose SSD (gp2)

The master database is not encrypted but all data in the new region must be encrypted: Encrypt a snapshot from the master DB instance, create a new encrypted master DB instance, and then create an encrypted cross-region Read Replica

tightly-coupled High Performance Computing (HPC) : ELASTIC FABRIC ADAPTOR
