# Elastic Compute Cloud
![[Pasted image 20230405130612.png]]
- Rent a virtual, remote machine
- Fully configurable, run any kind of workload on the cloud
- Can use [[VPC]]s alongside [[Security Group]]s for what goes in and out
- Usage
	- Config: Region -> OS -> Instance type -> Network Settings -> Config more settings -> **Launch**
	- Connect to instance -> Install software, add code -> Start workload / application -> (moniter workload) -> **Stop / Shut Down instance**
- Data such as the base OS and software is stored at either the [[EC2 Instance Store]] or is [[EBS]]-Backed (*default*)
- [[AMI]] --> Pre-configured [[EC2]] instance
- check [[EC2 Launch Template]]

#### Connection Options
- *EC2 Instance Connect* --> Accessible directly from inside the management console
	- Get a browser-based command line tool interface which allows you to run commands on teh EC2 instance
- *SSH Client and Key Pair* --> Can connect to a running EC2 instance via any SSH client, as long as you have a valid key pair
	- The key pair must be created / assigned during instance creation
	- Need the private key that is created in order to connect with a SSH client

#### Types:
1. *General Purpose* --> Provide a balance of compute, memory and networking resources, and can be used for a variety of diverse workloads
2. *Compute Optimized* --> Instances that are optimized for compute-intensive workloads
3. *Memory Optimized* --> Instances that are optimized for memory-intensive workloads **(Database)**
4. *Storage Optimized* --> Instances that are optimized for storage-intensive workloads **(Storage)**
5. *Accelerated Computing* --> A unique set of instance types that use specialized hardware accelerators or co-processors for operations like graphics processing, machine learning, or high performance computing


# Pricing
- **On Demand Instances** = *Default* and most flexible option
	- No Discounts
	- Price depends on chosen config
	- Pay for usage
- **Spot Instances** = Must be *manually selected* for usage (from advanced details)
	- Uses spare, currently not-in-use instances, can be reclaimed by any other user
	- Discount over on-demand pricing
	- Price depends on chosen config
	- Ideal for workloads that can be interrupted
- **Savings Plan** = Must be *bought separately*
	- Discount over on-demand pricing
	- Can be used with any other compute service, other than **EC2**
	- Pay in advance for a *chosen amount of usage*
	- Ideal if you can commit long-term
- **Reserved Instances** = Must be *bought separately*
	- Will be **either 1 or 3 years**
	- Discount over on-deman pricing
	- Pay in advance *for chosen instance types* 
		- *Example:* pay in advance for a t2.micro instance in advance, commiting for 1 or 3 years, and whenever starting such instance, which meets those reserved instance requirements set in advance, you wont get charged
	- Not very flexible (unlike the *savings plan*, which can choose any instance type), and only for **EC2**
