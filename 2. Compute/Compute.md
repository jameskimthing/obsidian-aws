#organize 
![[Pasted image 20230405130910.png]]
# Compute
- [[EC2]] for renting a virtual (remote) computer
- [[Elastic Beanstalk]] for auto-scaling, and more features (is a layer above [[EC2]])
- [[Lightsail]] for working with a simpler management console

## Containerized Workloads
![[Pasted image 20230405130920.png]]
- Check [[Containers]]
- Services that help with deploying, running, managing & scaling containerized applications in clusters
- For a simpler experience, check [[App Runner]]
- For using with the CLI, check [[Copilot]]

#### Images
- The "blueprint" for deploying containers, check [here](https://stackoverflow.com/questions/23735149/what-is-the-difference-between-a-docker-image-and-a-container) for more info
- **Storage**
	- Locally --> No remote repository (storage) needed
	- Server --> Stored in a distributed server (e.g.  [[ECR]] or [Docker Hub](https://hub.docker.com/))
- [[ECS]] && [[EKS]] --> For managing multiple [[Containers]] / kubernetees

#### Define Cluster Structure
- Define tasks: images & image configurations
- Choose an [[EC2]] instance or [[Fargate]] (for serverless) as the container host
- Configure default network && security settings

#### Operate && Scale Containers
- Define service / task specific settings
- Monitor containers

## Serverless!
![[Serverless.png]]
- Check [[Serverless]]
- [[Lambda]] is the main serverless service, but *compute is not everything*
- [[S3]] can be thought of as a serverless storage service

## Manage Compute Workflows
- [[Batch]] for planning && performing batch jobs
- [[Compute Optimizer]] for optimizing compute resources
- [[Systems Manager]] to gain operational insights into AWS and on-premises resource

