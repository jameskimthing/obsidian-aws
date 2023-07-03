# AWS Batch
![[Batch.png]]
- Efficiently runs hundreds of thousands of batch and ML computing jobs
- White optimizing compute resources
- Used, so you can focus on analyzing results and solving problems

#### Usage
- **Create Job Definition**
	- Define [[Fargate]] / [[EC2]] instance jobs
	- Define image (check [[Containers]]) / basic hardware requirements
	- Extra config: permissions, file systems, etc...
- **Execute Jobs**
	- Submit / schedule jobs
	- AWS provisions resources && execute jobs
	- Jobs && job status can be tracked