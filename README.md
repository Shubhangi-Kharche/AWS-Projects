*AWS Projects*
**AWS Project1**
**Team Communication Solution**
Implementing a Team Communication Solution using Mattermost and AWS. This is a scalable solution that can be hosted on a on-premises data center or on a public cloud,with its servers, storage etc. completely managed and controlled by your IT team in accordance with a company’s governance and security requirements.

Skills and Tools

EC2, VPC, Security Group, NAT Gateway / NAT Instance

Scenario

Team communication and instant messaging solutions are an integral part of any business environment today. As of 2020, the total number of users of Slack and Microsoft Teams exceeded 20 million. 

Some organizations might have compliance policies in place which do not allow them to use services managed by third parties. They will prefer solutions that can be managed and hosted on servers controlled by them. The same will extend to communication solutions as well.

Architecture Implementation
Implement 2 different subnets (one public and the other private) in a custom VPC
Install and configure MySQL on an Amazon Linux 2 instance on the private subnet using the instructions provided. (Hint: Use a bastion host and a NAT gateway)
Install and configure Mattermost on an Amazon Linux 2 instance on the public subnet using the provided instructions.
Configure the security groups to allow the ports as shown in the architecture.
Test the installation by accessing the IP of the public instance in a browser via the port 8065.

**AWS Project2****
**Building an Automated Business Process using Managed Services on a Public Cloud**
In the connected world, it is imperative that the organizations be interlinked with the customers and vendors. This process has been very sluggish, manual, batch-based and prone to failures. Such Integration design has lead to impaired decision-making and delays in the detection of fraudulent actions. This project created an automated, event-based real-time process using managed cloud services that do not have these limitations.

Skills and Tools

AWS S3, AWS SNS, AWS RDS, Python, Boto3

Architecture Implementation
The customer uploads the invoice data to S3 bucket in a text format as per their guidelines and policies. This bucket will have a policy to auto delete any content that is more than 1 day old (24 hours).
An event will trigger in the bucket that will place a message in SNS topic
A custom program running in EC2 will subscribe to the SNS topic and get the message placed by S3 event
The program will use S3 API to read from the bucket, parse the content of the file and create a CSV record and save the details in an RDS database
The program will use S3 API to write CSV record to destination S3 bucket as new S3 object.

**AWS Project3****
**Create and Manage a Nonrelational Database using AWS DynamoDB**

DynamoDB is a NoSQL database, allowing for flexible schema design that can evolve with your application. It provides low-latency performance with near-infinite scaling, so you do not need to worry about performance bottlenecks as your application grows. Create DynamoDB tables with required secondary keys and perform CRUD operations. Use Python and Boto 3, AWS SDK for Python, for ineracting with the DynamoDB APIs

Skills and Tools

DynamoDB, NoSQL, Python, Boto3, EC2
Scenario:

Testing/development of a cloud-native application on the cloud might not be feasible due to cost constraints. Therefore, when working on an application using DynamoDB as the back-end, we have to deploy it on-prem first for debugging purposes. 

This project deploys DynamoDB using an IaaS deployment on EC2 instances. This easily be adapted to an on-premise installation for testing and debugging purposes.

Objectives
1	Install DynamoDB on an EC2 instance as an IaaS installation
2	Connect to the IaaS DynamoDB installation using the given Python Script to perform CRUD operations
3	Run a Python Program to create a DynamoDB table in your AWS account with secondary indexes. 

**AWS Project4****
**Deploying web app using ECS**
In the last decades, small and large enterprises have invested heavily in developing bespoke applications. Since these applications have been built and enhanced over a period of time, they are complex and any form of re-engineering to convert it to smaller, modular and independently hosted services is difficult. Managed Container Services from cloud providers allows predictable and reproducible packaging of such apps. This project moved & deployed a classical web app to AWS ECS containers.

Skills and Tools

Docker, ECS, LoadBalancer, Fargate

Scenario

The introduction of Lambda support for OCI container images provides customers with more choices when it comes to packaging formats. Developers can now choose to take advantage of the event-driven runtime model and cost-savings advantages of AWS Lambda, while taking advantage of the predictability and control offered by a container-based development and deployment cycle.

Architecture Implementation
Package the web application as a Docker image running on Alpine with Python
Create an ECR repository and login to it.
Build the image with the downloaded dockerfile and the support files
Tag the image appropriately and push it into the ECR repository.
Create a Lambda function with the image in ECR.




