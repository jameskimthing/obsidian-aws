#organize 
![[Management Governance.png]]
# Management Governance
- Managing the cloud
- [[OpsWorks]] --> A web-based service that provides a graphical user interface (GUI) for managing and configuring applications in the AWS cloud

## Managing Multiple AWS Accounts
- It is possible to have 1 account, and multiple [[IAM]] accounts
- *Alternative:* Multiple accounts (with 1 or more [[IAM]] users each)
	- Use account limits multiple times (e.g. max number of *Elastic IPs*)
	- Use free tier / monthly free usage multiple times (e.g. monthly free lambda executions)
	- Improve organization && management by splitting by workload, team, or other criteria
- [[Organizations]] --> Centralized billing, centralized management, cross-account service configurations && more
- [[Control Tower]] (new!) --> Creates best-practice multi-account practice for you
- Share resources via [[RAM]]

## Financial Management
![[Financial Management.png]]
- [[Cost Explorer]]--> View bills (updated daily) and analyze costs with cost management tools
- [[Budgets]] --> Set budgets, get alarms when threshold exceeded
- [[Cost and Usage Report]] --> Can receive reports that break down your costs by the hour, day, or month, by product or product resource, or by tags that you define yourself
*Alternate way to view:*
- [[Cost Explorer]] --> Visualize costs over time
- [[Budgets]] --> Alarms on threshold


## Infrastructure as Code
- [[CloudFormation]] --> Automate infrastructure deployments & updates

## Service && Workload Configuration
- [[Systems Manager]] --> Manage workloads centrally
	- Manage application parameters via [[AppConfig]] / [[Parameter Store]]
	- Manage server fleets froma  central place (e.g. issue commands, updates, changes)
- Define && Share **Standardized Cloud Resources**
	- (Accounts shouldn't create different, custom solutions)
	- [[Launch Wizard]] --> Helps with launching standardized, pre-built (by AWS) applications
	- [[Proton]] --> Create standardized [[Serverless]] and [[Containers]] deployments
	- [[Service Catalog]] --> Create standardized configurable aws usage templates
	- [[RAM]] --> For shared resources
- Control **Service Configuration**
	- AWS [[Config]] --> Enforce service configurations
	- [[License Manager]] --> Manage software license

## Monitoring
- Keeping track of your services && applications
- Allows u to react && fix issues early

## Services
- [[CloudWatch]] --> *monitoring*
	- Provides a reliable, scalable, and flexible monitoring solution that you can start using within minutes
	- No longer need to set up, manage, and scale your own monitoring systems and infrastructure
- [[CloudTrail]] --> *auditing*
	- Audits your AWS deployments in the cloud by getting a history of AWS API calls
- [[XRay]] --> *tracing* (see the flow)
	- A distributed tracing system that enables you to understand the flow of requests and responses through your application
- [[XRay]] is more for debugging, while [[CloudWatch]] is just for monitoring, feeding its data into various sources


## Disaster Recovery and Prevention
- Coming back to live after a disaster
- [[Backup]] --> For backup
- [[Disaster Recovery Options]] --> Trades between *cost vs time* for recovery / prevention
- [[RTO && RPO]] --> Recovery time, and data loss

