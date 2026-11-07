---
title: "Week 2 Worklog"
date: 2026-10-12
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---


### Week 2 Objectives:

* Connect and get acquainted with the members of First Cloud AI Journey.
* Understand basic AWS services and how to use the Console & CLI.
* Learn how to manage costs and secure an AWS account.
* Build foundational knowledge of access management (IAM) and networking (VPC).

### Tasks to be carried out this week:
| Day | Tasks | Start Date | End Date | Reference |
| --- | ----- | ---------- | -------- | --------- |
| Mon | - Get acquainted with FCAJ members <br> - Read and note the internship unit's rules and regulations | 12/10/2026 | 12/10/2026 | |
| Tue | - Learn about AWS and its service types <br>&emsp; + Compute <br>&emsp; + Storage <br>&emsp; + Networking <br>&emsp; + Database <br>&emsp; + Security & Identity (IAM) <br>&emsp; + Management & Monitoring (CloudWatch, AWS Budgets) <br>&emsp; + Developer Tools (AWS CLI, Cloud9) <br>&emsp; + Containers (Lightsail Containers) <br> - Learn about Region, Availability Zone, Edge Location <br> - Learn about the Shared Responsibility Model | 13/10/2026 | 13/10/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Wed | - Create an AWS Free Tier account <br> - Learn about the AWS Console & AWS CLI <br> - **Hands-on:** <br>&emsp; + Create an AWS account <br>&emsp; + Install & configure AWS CLI <br>&emsp; + How to use AWS CLI <br> - Enable MFA for the root user <br> - **Hands-on:** Managing Costs with AWS Budgets <br>&emsp; + Create a Cost Budget & configure email alerts <br> - Learn about AWS Support: Basic/Developer/Business plans, how to create a support case | 14/10/2026 | 14/10/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Thu | - Learn EC2 basics: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + Key pair <br>&emsp; + Security Group <br>&emsp; + Instance Store and comparison with EBS <br>&emsp; + Pricing models: On-Demand, Reserved, Spot <br>&emsp; + User Data (script that runs when an instance starts) <br> - Ways to remote SSH into EC2 <br> - Learn about Elastic IP <br> - **Hands-on:** Access Management with IAM <br>&emsp; + Create IAM users, groups, policies <br>&emsp; + Learn the Least Privilege principle <br> - Learn VPC basics: VPC, Subnet, Route Table, Internet Gateway, Security Group | 14/10/2026 | 14/10/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Fri | - **Hands-on:** <br>&emsp; + Create an EC2 instance <br>&emsp; + Connect via SSH <br>&emsp; + Attach an EBS volume <br>&emsp; + Attach an IAM Role to EC2 (Instance Profile) <br> - Clean up resources: terminate EC2, delete EBS volume, release Elastic IP | 15/10/2026 | 16/10/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 2 Achievements:

* Understood what AWS is and grasped the basic service groups:
  * Compute
  * Storage
  * Networking
  * Database
  * Security & Identity (IAM, AWS Organizations)
  * Management & Monitoring (CloudWatch, CloudTrail, AWS Budgets)
  * Developer Tools (AWS CLI, Cloud9)
  * Containers (Lightsail Containers, ECS, EKS)
  * Understood the pay-as-you-go pricing model and the Free Tier

* Understood AWS's global infrastructure (Region, AZ, Edge Location) and the Shared Responsibility Model.

* Successfully created and configured an AWS Free Tier account.

* Enabled MFA for the root user to improve account security.

* Set up AWS Budgets to track costs and receive alerts when thresholds are exceeded.

* Understood the AWS Support plans and how to create a support case when help is needed.

* Became familiar with the AWS Management Console and learned how to find, access, and use services from the web interface.

* Grasped IAM basics:
  * Create users, groups, policies
  * Apply the Least Privilege principle
  * Distinguish between the root user and IAM users

* Installed and configured AWS CLI on the computer, including:
  * Access Key
  * Secret Key
  * Default Region
  * Output format (json, table, text)
  * Verifying the configuration with `aws configure list` and `aws sts get-caller-identity`

* Used AWS CLI to perform basic operations such as:

  * Checking account information & configuration
  * Listing regions
  * Viewing EC2 services
  * Creating and managing key pairs
  * Checking information about running services
  * Listing and checking the status of EC2 instances (`aws ec2 describe-instances`)
  * Listing Security Groups, VPCs, Subnets (`aws ec2 describe-security-groups`, `describe-vpcs`, `describe-subnets`)
  * Viewing the list of IAM users (`aws iam list-users`)
  * Using the `--query` and `--output` parameters to filter and format results

* Understood foundational VPC knowledge: Subnet, Route Table, Internet Gateway, Security Group.
  * Distinguished between Public Subnet and Private Subnet
  * Distinguished between Security Group and Network ACL
  * Understood CIDR blocks and how to divide IP ranges

* Practiced with EC2: used an IAM Role (Instance Profile) instead of an Access Key when EC2 needs to access other AWS services.
  * Created an instance and connected via SSH using a key pair (.pem)
  * Attached and mounted an EBS volume
  * Assigned an Elastic IP to the instance

* Learned to clean up resources after practice to avoid unexpected charges.
  * Terminate the EC2 instance
  * Delete unused EBS volumes and snapshots
  * Release the Elastic IP

* Able to connect the web interface and CLI to manage AWS resources in parallel.
  * Create resources on the Console, then verify them with the CLI