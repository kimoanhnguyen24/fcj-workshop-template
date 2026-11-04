---
title: "Week 4 Worklog"
date: 2026-10-27
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---


### Week 4 Objectives:

* Gain a deeper understanding of AWS IAM: the request authentication process, the Assume Role mechanism, and restricting access with Conditions.
* Practice creating IAM Groups, Users, and Roles, and restricting role switching by IP address and time.
* Understand how to package and deploy applications with Docker (Docker images, Docker Compose).
* Practice deploying a containerized application on AWS with EC2 and RDS, and storing images on Amazon ECR and Docker Hub.

### Tasks to be carried out this week:
| Day | Tasks | Start Date | End Date | Reference |
| --- | ----- | ---------- | -------- | --------- |
| Mon | - Learn advanced AWS IAM <br>&emsp; + The process of sending a request to an AWS service <br>&emsp; + How AWS authenticates requests <br>&emsp; + The Assume Role process <br>&emsp; + The Least Privilege principle when granting admin permissions <br> - Learn about IAM Role Conditions: restricting access by IP address and by time | 23/10/2026 | 23/10/2026 | <https://000044.awsfcaj.com/> |
| Tue | - **Hands-on:** IAM Role & Condition <br>&emsp; + Create an IAM Group <br>&emsp; + Create an IAM User <br>&emsp; + Verify the user's permissions <br>&emsp; + Create an Admin IAM Role <br>&emsp; + Configure Switch role <br>&emsp; + Limit switch role by IP <br>&emsp; + Limit switch role by time <br>&emsp; + Clean up resources | 24/10/2026 | 24/10/2026 | <https://000044.awsfcaj.com/> |
| Wed | - Learn about Docker: containers, Docker images, Docker Hub, Amazon ECR <br> - Learn the architecture for deploying Docker applications on AWS (EC2, RDS, ECR) <br> - Learn about DB Subnet Groups, Amazon RDS, and the IAM Role that allows EC2 to access ECR <br> - **Hands-on:** Deploy Application on Docker <br>&emsp; + Install dependencies on the local machine <br>&emsp; + Deploy the application locally <br>&emsp; + Test the application | 25/10/2026 | 25/10/2026 | <https://000015.awsfcaj.com/> |
| Thu | - **Hands-on:** Deploy Application on Docker <br>&emsp; + Configure the VPC and Security Groups <br>&emsp; + Create an IAM Role for ECR access <br>&emsp; + Log in to Docker Hub <br>&emsp; + Create a DB Subnet Group <br>&emsp; + Launch an RDS Instance <br>&emsp; + Configure and launch an EC2 Instance <br>&emsp; + Install the required libraries on EC2 <br>&emsp; + Add data to the database for testing | 26/10/2026 | 26/10/2026 | <https://000015.awsfcaj.com/> |
| Fri | - Learn how to deploy an application using only a Docker image <br> - Learn about Docker Compose and managing multiple containers <br> - Learn how to store and distribute images with Amazon ECR and Docker Hub <br> - **Hands-on:** Deploy Application on Docker <br>&emsp; + Deploy the application with a Docker image and test it <br>&emsp; + Deploy the application with Docker Compose and test it <br>&emsp; + Push the image to Amazon ECR <br>&emsp; + Push the image to Docker Hub <br>&emsp; + Clean up resources | 27/10/2026 | 27/10/2026 | <https://000015.awsfcaj.com/> |


### Week 4 Achievements:

* Gained a deeper understanding of AWS IAM:
  * Understood the process of sending requests to AWS services and how AWS authenticates requests
  * Understood the Assume Role process and the role of an IAM Role in granting temporary permissions
  * Applied the Least Privilege principle when granting per-service admin permissions

* Practiced IAM Role & Condition:
  * Created an IAM Group and IAM User and verified access permissions
  * Created an Admin IAM Role and configured Switch role
  * Restricted role switching by IP address
  * Restricted role switching by time period
  * Cleaned up resources after practice

* Understood the basic concepts of Docker:
  * Containers, Docker images, Docker Hub, Amazon ECR
  * The difference between direct deployment and container-based deployment

* Practiced deploying an application with Docker:
  * Installed dependencies, deployed, and tested the application on the local machine
  * Prepared the AWS infrastructure: VPC, Security Groups, IAM Role for ECR access
  * Created a DB Subnet Group and launched an Amazon RDS Instance
  * Configured an EC2 Instance, installed libraries, and added test data to the database
  * Deployed the application using a Docker image
  * Deployed the application using Docker Compose

* Practiced managing Docker images:
  * Pushed an image to Amazon ECR
  * Pushed an image to Docker Hub
