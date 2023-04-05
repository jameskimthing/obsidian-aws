# Elastic Beanstalk
![[Pasted image 20230405130623.png]]
- Is one layer of abstraction away from the [[EC2]] layer
- Will setup an *environment* for you that can contain:
	- A number of [[EC2]] instances
	- An optional database
	- A few other AWS components such as a:
		- [[ELB]]
		- *Auto-Scaling Group* (check [[EC2 Auto Scaling]]])
		- [[Security Group]]
- Then will manage these items for you whenever you want to update your software running in AWS
- Doesn't add any cost on top of these resources that it creates for you
	- e.g. If you have 10 hours of [[EC2]] usage, then all you pay is 10 compute hours

#### Usage
- **Create Applications && Environments**
	- Define programming language && environment
	- Choose a preset && adjust as needed
	- Configure instance types, security settings, && more
- **Scaling**
	- Add load balancing (ex: [[ELB]]) as needed
- **Database**
	- Add a connected database in the same creation wizard
- **Configure updates && deployments**

