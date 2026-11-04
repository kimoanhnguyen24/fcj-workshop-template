---
title: "Week 3 Worklog"
date: 2026-10-20
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---


### Week 3 Objectives:

* Understand how to build a hybrid DNS system between on-premises DNS and Amazon Route 53 using Route 53 Resolver.
* Practice deploying Microsoft AD and configuring Outbound Endpoints, Inbound Endpoints, and Resolver Rules.
* Understand and use Amazon CloudWatch to monitor resources: Metrics, Logs, Alarms, Dashboards.
* Learn how to analyze logs and set up alerts to monitor systems.

### Tasks to be carried out this week:
| Day | Tasks | Start Date | End Date | Reference |
| --- | ----- | ---------- | -------- | --------- |
| Mon | - Learn about Amazon Route 53 and Route 53 Resolver <br>&emsp; + Route 53 capabilities: domain registration, private DNS zones, hybrid DNS, name resolution <br>&emsp; + The 3 components of hybrid DNS: Outbound Endpoint, Inbound Endpoint, Resolver Rules <br>&emsp; + Overall architecture of the Hybrid DNS lab <br> - **Hands-on:** <br>&emsp; + Generate a Key Pair <br>&emsp; + Initialize the infrastructure with a CloudFormation Template <br>&emsp; + Configure Security Groups | 16/10/2026 | 16/10/2026 | <https://000010.awsfcaj.com/> |
| Tue | - Learn the role of the RDGW (Remote Desktop Gateway) and Microsoft AD in the simulated on-premises DNS model <br> - Learn how the Route 53 Outbound Endpoint works (sending DNS queries from AWS to the on-premises DNS) <br> - **Hands-on:** <br>&emsp; + Connect to the RDGW <br>&emsp; + Deploy Microsoft AD <br>&emsp; + Create a Route 53 Outbound Endpoint | 17/10/2026 | 17/10/2026 | <https://000010.awsfcaj.com/> |
| Wed | - Learn about Route 53 Resolver Rules (forwarding queries for specific domains) <br> - Learn about the Route 53 Inbound Endpoint (receiving DNS queries from on-premises) <br> - Learn the two-way DNS query flow between AWS and on-premises <br> - **Hands-on:** <br>&emsp; + Create Route 53 Resolver Rules <br>&emsp; + Create a Route 53 Inbound Endpoint <br>&emsp; + Verify two-way domain name resolution <br>&emsp; + Clean up resources | 18/10/2026 | 18/10/2026 | <https://000010.awsfcaj.com/> |
| Thu | - Learn about Amazon CloudWatch <br>&emsp; + Overview: collecting and analyzing metrics and logs in one unified place <br>&emsp; + CloudWatch Metrics: Search expressions, Math expressions, Dynamic Labels <br>&emsp; + CloudWatch Logs: log groups, log streams <br> - **Hands-on:** <br>&emsp; + Prepare the lab environment <br>&emsp; + CloudWatch Metrics: view metrics, Search expressions, Math expressions, Dynamic Labels <br>&emsp; + CloudWatch Logs: view and manage log groups and log streams | 19/10/2026 | 19/10/2026 | <https://000008.awsfcaj.com/> |
| Fri | - Learn about CloudWatch Logs Insights (log query syntax) and Metric Filters <br> - Learn about CloudWatch Alarms (thresholds, alarm states, notification actions) <br> - Learn about CloudWatch Dashboards <br> - **Hands-on:** <br>&emsp; + Use Logs Insights to query and analyze logs <br>&emsp; + Create a Metric Filter from logs <br>&emsp; + Create an Alarm and configure notifications <br>&emsp; + Build a consolidated Dashboard <br>&emsp; + Clean up resources | 20/10/2026 | 20/10/2026 | <https://000008.awsfcaj.com/> |


### Week 3 Achievements:

* Understood Amazon Route 53 and Route 53 Resolver:
  * Distinguished Route 53 capabilities: domain registration, private DNS zones, hybrid DNS, name resolution
  * Understood the role of the Outbound Endpoint (sending DNS queries from AWS to the on-premises DNS)
  * Understood the role of the Inbound Endpoint (receiving DNS queries from on-premises for domains on AWS)
  * Understood Resolver Rules (forwarding queries for specific domains to the on-premises DNS)

* Practiced setting up Hybrid DNS:
  * Generated a Key Pair, initialized infrastructure with CloudFormation, and configured Security Groups
  * Connected to the RDGW and deployed Microsoft AD
  * Created an Outbound Endpoint, Resolver Rules, and an Inbound Endpoint
  * Verified name resolution between the on-premises environment (Microsoft AD) and AWS
  * Cleaned up resources after completion

* Understood Amazon CloudWatch and its role in system monitoring:
  * Collected and analyzed metrics and logs in one unified place
  * Understood end-to-end observability and automated actions based on alerts

* Practiced CloudWatch Metrics:
  * Viewed and looked up metrics of AWS resources
  * Used Search expressions to find multiple metrics at once
  * Used Math expressions to perform calculations on metrics
  * Used Dynamic Labels to display meaningful labels on graphs

* Practiced CloudWatch Logs:
  * Managed log groups and log streams
  * Used Logs Insights to query and analyze logs
  * Used Metric Filters to turn log data into metrics

* Practiced CloudWatch Alarms and Dashboards:
  * Created threshold-based alarms and configured notifications
  * Built a dashboard for centralized tracking of key indicators
