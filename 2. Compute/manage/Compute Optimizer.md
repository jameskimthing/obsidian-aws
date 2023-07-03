![[Compute Optimizer.png]]
# Compute Optimizer
- Helps avoid overprovisioning and underprovisioning four types of AWS resources:
	- [[EC2]] instance types
	- [[EBS]] volumes
	- [[ECS]] services on [[Fargate]]
	- [[Lambda]] functions
- Based on your utilization data

- Uses machine learning to analyze [[CloudWatch]] metrics && resource configurations
- Recommends improvements (e.g. use a different instance type / memory settings)