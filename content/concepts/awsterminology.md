---
title: "AWS Basic Terminologies"
date: 2020-07-24T00:10:26-04:00
draft: false
---

##### Terminology credits : intellipaat.com

## Networking Services
- **VPC**: Amazon Virtual Private Cloud (VPC) is a virtual data center in AWS consisting of a set of isolated resources.
- **Direct Connect**: It is used to establish a dedicated network connection from the host network to AWS without an Internet connection.
- **Route 53**: It is a scalable and highly available Domain Name System (DNS) and domain name registration service, and 53 is the port on which this service runs.

## Computing Services
- **EC2**: It is a virtual server that provides resizable compute capacity on the cloud.
- **Elastic Beanstalk**: It is an application container used for deploying and managing containers. It creates an environment for working with web applications.
- **Lambda**: It is a computing service that runs the code in response to events and automatically manages the computing resources.
- **EC2 Container Service**: It allows us to easily run and manage Docker containers across a cluster of EC2 instances.

## Storage Services
- **S3**: It refers to Simple Storage Service and allows the storage of data objects of any sort and flat files in the cloud. It is secure, scalable, and durable.
- **CloudFront**: It defines a Content Delivery Network. It provides a way to distribute content to end-users with low-latency and high data-transfer speeds.
- **Glacier**: It is a low-cost storage service that provides secure and durable storage for long-term data archiving and backup.
- **EFS (Elastic File Storage)**: It is a file storage service used in EC2 instances and connects to multiple EC2 instances.
- **Snowball**: It is used for moving large amounts of data into/out of AWS using secure appliances, i.e., it provides the data archiving functionality for the data that no longer needs to be accessed actively.
- **Storage Gateway**: It is used for securely integrating on-premises IT environments with cloud storage for backup and disaster recovery.


## Database
- **RDS (Relational Database Service)**: It allows the storage of data objects as part of the relational database. It makes it easy to set up, operate, and scale familiar relational databases in the cloud.
- **DynamoDB**: It is a scalable NoSQL data store that is used to manage distributed replicas of data for high availability.
- **ElastiCache**: It improves application performance by allowing us to retrieve information from an in-memory caching system. It is a way of caching databases in the cloud.
- **Redshift**: It is a fast, fully managed data warehousing service, which makes it cost-effective to analyze all data using the existing Business Intelligence tools.
- **DMS (Data Migration Service)**: It helps in migrating databases to the cloud easily and securely. It can also be used for converting databases.


## Analytics
- **EMR**: Amazon Elastic MapReduce helps in performing big data tasks such as web indexing, data mining, and log file analysis.
- **Data Pipeline**: It helps in moving data from one service to another. It is a service used for periodic, data-driven workflows.
- **AWS Elasticsearch**: It is a managed service that helps in deploying, operating, and scaling Elasticsearch.
- **Kinesis**: It makes it easy to work with real-time streaming data in the AWS cloud.
- **AWS Machine Learnin**g: It is a service that enables us to easily build smart applications.
- **AWS QuickSight**: It is a cloud-assisted Business Intelligence service that helps in deriving insights from data easily.


## Security and Identity
- **IAM (Identity and Access Management)**: It helps in configuring security for all the services. It is used to ensure that our other services remain safe and inaccessible to others.
- ***Directory Service**: It is used to provide a managed directory in the cloud.
- **Inspector**: It enables us to analyze the behavior of the applications we run on AWS and helps in identifying potential security issues.
- **WAF (Web Application Firewall)**: It protects our web application from attacks by providing web traffic filters.
- **Cloud HSM**: It is a Hardware Security Module.
- **KMS (Key Management Service)**: It is a Key Management Service.


## Management Tools
- **CloudWatch**: It is used to create different metrics. It provides monitoring for resources and applications.
- **CloudFormation**: It helps in creating and updating a collection of related AWS resources.
- **CloudTrial**: It provides increased visibility into user activity by recording API calls made on an account.
- **OpsWorks**: It is a DevOps platform for managing applications of any size or complexity on the AWS cloud.
- **Config**: It gives an inventory of AWS resources, lets us audit the AWS resource configuration history, and notifies the changes.
- **Service Catalog**: It allows organizations to manage approved catalogs of IT resources.
- **Trusted Advisor**: It inspects the AWS environment and finds opportunities to save money and improve system performance.


## Application Services
- **API Gateway**: It is used to create, maintain, monitor, and secure APIs.
- **AppStream:** It is used to stream resource-intensive applications and games from the cloud to multiple users.
- **CloudSearch**: It is a completely managed search service for websites and apps.
- **Elastic Transcoder**: It is used to convert media files in the cloud easily at a lower cost.
- **SES (Simple Email Service)**: It is used to send and receive emails.
- **SQS (Simple Queue Service)**: It is a reliable, hosted queue for storing messages.
- **SWF (Simple Workflow Service)**: It is used to coordinate all the processing steps with an application.

## Developer Tools
- **Code commit**: It is a managed source-control service that hosts private Git repositories.
- **Code deploy**: It is used to automate the code deployment.
- **Code pipeline**: It is a continuous delivery service that enables us to visualize and automate the steps required to release software.


# S3 vs EBS vs EFS 
{{< figure src="/images/s3ebsefs.JPG" >}}