---
title: "Week 5 Worklog"
date: 2026-11-02
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Understand the Serverless model: how Lambda works in response to events, why there is no server to manage, and the role of each service in a Serverless web application.
* Understand how services interact: S3 triggering Lambda, Lambda writing data to DynamoDB, and the role of IAM Policies in granting permissions to Lambda.
* Understand AWS PrivateLink and VPC Endpoints: why AWS services should be accessed without traversing the public Internet.
* Distinguish Gateway Endpoints from Interface Endpoints in terms of routing mechanism, use cases, and security controls.
* Understand the challenge of accessing S3 from on-premises (hybrid) environments and the DNS issues that come with it.
* Understand VPC Endpoint Policies and how to combine them with bucket policies to control access.
* Complete the labs to verify the knowledge gained.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 | - Learn about Serverless Computing <br>&emsp; + Concept: running code, managing data, and integrating applications without managing server infrastructure <br>&emsp; + Comparison with the traditional model (self-managed EC2) <br> - Learn about Serverless web application architecture on AWS <br>&emsp; + AWS Lambda: processing logic <br>&emsp; + Amazon DynamoDB: data storage <br>&emsp; + Amazon API Gateway: handling user requests <br>&emsp; + S3 / AWS Amplify: hosting static web applications <br> - Learn about the overall architecture of the Book Store application in the series <br>&emsp; + User features: register, log in, browse books, add to cart, checkout <br>&emsp; + Admin features: add, edit, delete books, manage orders <br>&emsp; + Related services in the series: Cognito, SNS, SQS, API Gateway | 02/11/2026 | 02/11/2026 | <https://000078.awsfcaj.com/> |
| 3 | - Learn about AWS Lambda <br>&emsp; + Lambda functions are invoked by events (event-driven) <br>&emsp; + Trigger mechanism from S3 when a new object is uploaded <br>&emsp; + Execution role and IAM Policy allowing Lambda to access S3 <br>&emsp; + Applying the Least Privilege principle when granting permissions to Lambda <br> - Learn about Amazon DynamoDB <br>&emsp; + Concepts: table, item, attribute, primary key <br>&emsp; + Role of the Books table storing book information and the S3 bucket storing book images <br> - **Hands-on:** Image Processing and Optimization on AWS <br>&emsp; + Create a Lambda function for image processing <br>&emsp; + Create an S3 Bucket and an IAM Policy for Lambda <br>&emsp; + Test the Lambda function | 03/11/2026 |03/11/2026 | <https://000078.awsfcaj.com/> |
| 4 | - Learn how Lambda writes data to DynamoDB <br>&emsp; + Permissions required for Lambda to write to a table <br>&emsp; + Data flow: S3 / Lambda / DynamoDB <br> - **Hands-on:** Writing Data to Amazon DynamoDB <br>&emsp; + Create a DynamoDB Table <br>&emsp; + Create a Lambda function to write data <br>&emsp; + Clean up resources (delete the Books table, empty and delete the S3 Bucket, delete the Lambda function) <br> - Learn about AWS PrivateLink <br>&emsp; + Private connectivity from VPCs and on-premises networks to AWS services <br>&emsp; + Traffic does not traverse the public Internet <br>&emsp; + Why an Internet Gateway or NAT Gateway is not required to access S3 | 04/11/2026 | 04/11/2026 | <https://000078.awsfcaj.com/> <br> <https://000111.awsfcaj.com/> |
| 5 | - Learn about the types of VPC Endpoints <br>&emsp; + Gateway Endpoint: used for S3 and DynamoDB, routes traffic through route tables using private IPs <br>&emsp; + Interface Endpoint: uses an ENI with a private IP in the subnet, resolved via DNS, controlled with Security Groups <br>&emsp; + Gateway Load Balancer Endpoint: forwards traffic to security appliances <br> - Learn about accessing S3 from on-premises <br>&emsp; + Hybrid connectivity via AWS Direct Connect or Site-to-Site VPN <br>&emsp; + Why Gateway Endpoints cannot be used from on-premises <br>&emsp; + Solution: S3 Interface Endpoint <br> - Learn about DNS issues when accessing S3 through an Interface Endpoint <br>&emsp; + Using endpoint-specific DNS names or the --endpoint-url parameter <br>&emsp; + Configuring on-premises DNS to resolve S3 domain names to endpoint IPs (Route 53 Resolver Inbound Endpoint, private hosted zone) <br>&emsp; + Note: endpoint IPs can change when subnets are added or removed <br> - **Hands-on:** Access S3 from VPC <br>&emsp; + Prepare the environment, create and test a Gateway Endpoint | 05/11/2026 | 05/11/2026 | <https://000111.awsfcaj.com/> |
| 6 | - Learn about VPC Endpoint Policies <br>&emsp; + An IAM resource policy attached to the endpoint, separate from the user's IAM policy <br>&emsp; + Restricts which buckets and principals can be accessed through the endpoint <br>&emsp; + Combined with bucket policies to allow access only from specific endpoints <br> - Learn about endpoint deployment architectures <br>&emsp; + Centralized endpoints vs. endpoints placed in each individual VPC <br>&emsp; + Cost and security benefits of using VPC Endpoints <br> - **Hands-on:** Access S3 from on-premises <br>&emsp; + Create and test an S3 Interface Endpoint <br>&emsp; + Simulate on-premises DNS <br> - **Hands-on:** VPC Endpoint Policies (bonus) and resource cleanup | 06/11/2026 | 06/11/2026 | <https://000111.awsfcaj.com/> |


### Week 5 Achievements:

* Understood the Serverless model:
  * Serverless lets you run code, manage data, and integrate applications without managing servers
  * Grasped the role of each component: Lambda (processing logic), DynamoDB (data storage), API Gateway (handling requests), S3/Amplify (hosting static web)
  * Understood the Book Store application architecture and how other services (Cognito, SNS, SQS, API Gateway) will be added in later parts of the series
* Understood how Lambda interacts with S3 and DynamoDB:
  * Lambda runs in response to events and is triggered by changes in S3
  * Lambda needs appropriate IAM Policies to read/write S3 and write to DynamoDB, granting only the permissions required (Least Privilege)
  * Understood the data flow: images uploaded to S3, processed by Lambda, book information stored in DynamoDB
* Understood AWS PrivateLink and VPC Endpoints:
  * Access AWS services privately without the public Internet, and without an Internet Gateway or NAT Gateway
  * Distinguished the 3 endpoint types: Gateway, Interface, Gateway Load Balancer
  * Gateway Endpoint: routed via route tables, supports only S3 and DynamoDB, usable only from within the VPC
  * Interface Endpoint: creates an ENI with a private IP, resolved via DNS, uses Security Groups, reachable from on-premises over Direct Connect/VPN
* Understood hybrid access to S3:
  * Why on-premises environments need an Interface Endpoint instead of a Gateway Endpoint
  * DNS issues and approaches to handle them: endpoint-specific DNS names, --endpoint-url, Route 53 Resolver Inbound Endpoint, private hosted zone
  * Considerations when using TLS/SSL and when endpoint IPs change
* Understood access control with VPC Endpoint Policies:
  * An endpoint policy is a separate resource policy attached to the endpoint
  * Combining endpoint policies and bucket policies to restrict access by bucket, principal, or specific endpoint
  * Knew the two endpoint deployment approaches: centralized and per-VPC
* Hands-on practice to verify knowledge:
  * Lambda processing images from S3 and writing data to DynamoDB
  * Created and tested a Gateway Endpoint and an Interface Endpoint, and simulated on-premises DNS
  * Configured a VPC Endpoint Policy and cleaned up resources after each lab