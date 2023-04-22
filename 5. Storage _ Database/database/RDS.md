# Relational Database Service
![[Pasted image 20230405131858.png]]
- A managed database service
- **IS NOT SERVERLESS**
- Choose the following:
	- **Database Engine**
		- Version of database
		- Auto-update settings
		- ![[RDS Engines.png|600]]
			- Check [[Aurora]] for info on the **Amazon Aurora** engine
	- **Hardware && Network Config**
		- Instance class (hardware profile)
		- [[VPC]], [[Subnets]], and  [[Security Group]]
	- **Database Server**
		- Login credentials and port
		- *Replication* for high availability && performance
			- ![[RDS Replication.png|500]]
		- Monitoring settings
		- Encryption && Backup Settings

