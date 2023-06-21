#organize 
# Migration && Hybrid
- At the highest level, the [AWS Cloud Adoption Framework (AWS CAF)](https://d1.awsstatic.com/whitepapers/aws_cloud_adoption_framework.pdf) organizes guidance into 6 areas of focus called **Perspectives**
	- In general
		- **Business**, **People**, and **Governance** --> on business capabilities
		- **Platform**, **Security**, and **Operations** --> on technical capabilities.

### The 6 R's
- The 6 strategies for migration
	- **Rehosting** --> “lift-and-shift” involves moving applications without changes
	- **Replatforming** --> “lift, tinker, and shift” involves making a few cloud optimizations to realize a tangible benefit.
		- Optimization is achieved without changing the core architecture of the application
	- **Refactoring** / **re-architecting** --> Involves reimagining how an application is architected and developed by using cloud-native features
		- Is driven by a strong business need to add features, scale, or performance that would otherwise be difficult to achieve in the application’s existing environment
	- **Repurchasing**  -->involves moving from a traditional license to a software-as-a-service model
		- *example:* a business might choose to implement the repurchasing strategy by migrating from a customer relationship management (CRM) system to Salesforce.com
	- **Retaining** --> Consists of keeping applications that are critical for the business in the source environment
		- Might include applications that require major refactoring before they can be migrated, or, work that can be postponed until a later time
	- **Retiring** --> The process of removing applications that are no longer needed


## Migration
![[Pasted image 20230405132520.png]]
- [[Migration Hub]] --> Track application migration process in a single location
- [[Application Migration Service]] --> Automate server application migration (agent software analyzes + replicates system) 
- [[DMS]] --> Automated database migration
- [[DataSync]] --> Simplify and accelerate secure data migrations
- [[Transfer Family]] --> A secure transfer service that enables you to transfer files into and out of AWS storage services
- [[Snow Family]] --> Physical devices for moving data and / or performing compute tasks (at the edge)


## Hybrid Cloud Computing
- [[Outposts]] --> Add AWS to on-premises
- [[Storage Gateway]] --> Interface for enabling on-premises workloads to use cloud storage
- [[Snow Family]] --> Portable devices, usable for data migration / edge computing
- [[DataSync]] && [[Transfer Family]] --> Service for syncing data between cloud & on premises
- [[ECS Anywhere]], [[EKS Anywhere]] --> Tooling & APIs for running [[ECS]] / [[EKS]] on local infrastructure
- [[Systems Manager]] --> Manage large-scale server fleets ([[EC2]] && local), parameters, incidents, && more
