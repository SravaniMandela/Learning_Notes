ECS : taskrolearn

scale independently : decouple (Sqs)

hybrid : storage gateway (on- premise capacity ran out u wanna store data both in on-prem and aws then use this)

prev : cloudfront to ALB now u want to access the content directly through the ELB then Create a VPC Security Group for the ELB and use AWS Lambda to automatically update the CloudFront internal service IP addresses when they change

data transformation : glue

Set an IAM permissions boundary on the developer IAM role that explicitly denies attaching the administrator policy

cloudfront distribution : WAF ACL and OAC

high performance computing (HPC): Fsx for lustre and s3 for cold data storage

RedShift is a columnar data warehouse DB that is ideal for running long complex queries. RedShift can also improve performance for repeat queries by caching the result and returning the cached result when queries are re-run

apply encryption to the database for all new and existing data.: Take a snapshot of the RDS instance. Create an encrypted copy of the snapshot. Restore the RDS instance from the encrypted snapshot

**you cannot create an encrypted read replica from an unencrypted database instance.**

at rest encryption : kms keys

uploaded to Amazon S3 standard storage class are initially accessed frequently for a period of 30 days. Then, objects are infrequently accessed for up to 90 days. After that, the objects are no longer needed.: **Transition to ONEZONE_IA after 30 days. After 90 days expire the objects**

highly resilient hybrid cloud architecture connecting an on-premises data center and AWS: Configure DX(direct connect) connections at multiple DX locations.

Put the JSON documents in an Amazon S3 bucket. As documents arrive in the S3 bucket, create an AWS Lambda function that runs Python code to process them. Use Amazon Aurora DB clusters to store the results.

A company has divested a single business unit and needs to move the AWS account owned by the business unit to another AWS Organization. How can this be achieved?**Migrate the account using the AWS Organizations console**

multiple AWS accounts : Transit gateway

block level storage and millions of req per sec : ec2 instance store

milli second retrieval : dynamodb

instances inside vpc should not access internet : Configure the route table for the private subnet so that it routes the outbound traffic to an AWS Network Firewall firewall then configure domain list rule groups.
