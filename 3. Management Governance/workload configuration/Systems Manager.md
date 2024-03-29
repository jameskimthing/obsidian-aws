![[Systems Manager.png]]
# Systems Manager
- A service with many capabilities that help with managing large fleets of servers & applications
- Check [[AppConfig]]

#### 4 Core Feature Groups
- **Node Management**
	- Group, visualize, && manage a fleet of servers
	- Connect to server via [[Systems Manager#Session Manager|Session Manager]]
	- Orchestrate patches && system-wide commands
- **Operations Management**
	- Manage server-wide operations
	- Manage incidents
	- Fleet monitoring
- **Application Management**
	- Manage application parameters
	- Provide && manage application configuration
	- Easily deploy or roll back configuration changes
- **Change Management**
	- Manage fleet changes && updates
	- Automate change requests
	- Configure standardized maintenance windows

### Systems Manager Agent (SSM Agent)
- Software that runs on [[EC2]] instances, [[Edge Devices]], on-premises servers, and virtual machines (VMs)
	- Makes it possible for [[Systems Manager]] to update, manage, and configure these resources
	- Processes requests from the [[Systems Manager]], then runs them as specified in the request


![[Session Manager.png]]
## Session Manager
- Can manage your [[EC2]] instances, [[Edge Devices]], on-premises servers, and virtual machines (VMs)

![[Parameter Store.png]]
## Parameter Store
- Provides secure, hierarchical storage for configuration data management and secrets management
- Can store data such as passwords, database strings, Amazon Machine Image ([[AMI]]) IDs, and license codes as parameter values
	- can be used to store *env* variables, too
- When storing *incredibly sensitive data*, use [[Secrets Manager]] instead


