#organize 
![[Management Governance.png]]
# Management Governance
- Managing the cloud
- Use [[Tags]] and [[Resource Groups]] to organize resources
- [[Well-Architected Framework]] --> Helps you understand the pros and cons of decisions you make while building systems on AWS
- [[Acceptable Use Policy]] --> Things you are not allowed to do with AWS

| Icon | Name | Description |
| --- | --- | --- |
| ![[Well Architected Tool.png]] | [[Well Architected Tool]] | Gives a catalog of questions, to be challenged, so that you are forced to evaluate your infrastructure |
| ![[Trusted Advisor.png]] | [[Trusted Advisor]] | Automatically perform some predefined checks && offer recommendations |


## Workload Configuration
- Use [[RAM]] for secure resource sharing

| Icon | Name | Description |
| --- | --- | --- |
| ![[OpsWorks.png]] | [[OpsWorks]] | Web-based service that provides a GUI for managing and configuring applications in the AWS cloud |
| ![[CloudFormation.png]] | [[CloudFormation]] | Automate infrastructure deployments & updates |
| ![[Launch Wizard.png]] | [[Launch Wizard]] | Helps with launching standardizes, pre-built (by AWS) applications |
| ![[Proton.png]] | [[Proton]] | Create standardized [[Serverless]] and [[Containers]] deployments |
| ![[Service Catalog.png]] | [[Service Catalog]] | Create standardized configurable AWS usage templates |
| ![[_icons/Config.png]] | [[Config]] | Enforce service configurations |
| ![[License Manager.png]] | [[License Manager]] | Manage software license |
| ![[Systems Manager.png]] | [[Systems Manager]] | Manage workloads centrally |
| ![[App Config.png]] | [[AppConfig]] | Feature of [[Systems Manager]], manage app parameters |
| ![[Parameter Store.png]] | [[Systems Manager#Parameter Store\|Parameter store]] | Feature of [[Systems Manager]], manage app parameters |


## Managing Accounts
- Can have multiple [[IAM]] accounts with a single "root" account
	- *or* can have multiple accounts with multiple [[IAM]] users each
		- Can use account limit mutiple times (e.g. max num of *Elastic IPs*)
		- Use free tier multiple times
		- Improve organization && management by splitting workload

| Icon | Name | Description |
| --- | --- | --- |
| ![[Organizations.png]] | [[Organizations]] | Centralized billing && management, cross account service config, etc... |
| ![[Control Tower.png]] | [[Control Tower]] | Simplified version of [[Organizations]] |
| ![[_icons/RAM.png]] | [[RAM]] | Securely share resources across accounts |
| ![[_icons/IAM.png]] | [[IAM]] | Managing accounts of the employees |
| ![[Identity Center.png]] | [[Identity Center]] | [[IAM]] users can use this for logging in |



![[Financial Management.png]]
## Financial Management
- [[Organizations]] / [[Control Tower]] --> Consolidated billing

| Icon | Name | Description |
| --- | --- | --- |
| ![[Cost Explorer.png]] | [[Cost Explorer]] | View bills updated daily, analyze costs with tools *(visualize costs over time)* |
| ![[Cost and Usage Report.png]] | [[Cost and Usage Report]] | Receive reports that break down cost by hour, day or month, by product / resource, by [[Tags]] |
| ![[Budgets.png]] | [[Budgets]] | Set budgets, get alarms when a threshold is reached |
| ![[CloudWatch Alarms.png]] | [[CloudWatch#CloudWatch Alarm\|CloudWatch Alarm]] | Billing alarms, but not as feature-rich as [[Budgets]] |  |


## Monitoring
- Keeping track of your services && applications
- Allows u to react && fix issues early
- Between [[CloudWatch]] and [[XRay]]
	- [[XRay]] --> More of debugging, "seeing the flow"
	- [[CloudWatch]] --> Monitoring, feeding its data into various sources

| Icon | Name | Description |
| --- | --- | --- |
| ![[CloudWatch.png]] | [[CloudWatch]] | *(monitoring)* Flexible monitoring solution |
| ![[CloudTrail.png]] | [[CloudTrail]] | *(auditing)* Logs all API calls between AWS services |
| ![[XRay.png]] | [[XRay]] | *(tracing)* Enables u to understand the flow of requests && responses throughout application |


## Disaster Recovery and Prevention
- Coming back to live after a disaster
- *RTO (Recovery Time Objective)* --> How quickly after an outage an application must be available again
- *RPO (Recovery Point Objective)* --> How much data loss u can tolerate
	- ![[Disaster Recovery Options.png|600]]

| Icon | Name | Description |
| --- | --- | --- |
| ![[Backup.png]] | [[Backup]] | For backup |

