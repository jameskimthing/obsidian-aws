# Elastic Block Store
![[Pasted image 20230405131909.png]]
- Attach a (virtual) **hard drive** to an [[EC2]] instance (**Exclusively for EC2 only**)
	- Multiple volumes can be added to at the same instance
	- Can be formatted and structured as needed (via the command line / code from inside the instance)
- An unformatted hard drive
- Create custom structure & store any files

#### Different Types
- SSD vs HDD
- Optimized for different workloads and tasks, such as access patterns

#### Elastic Volumes
- If needed, volumes can scale dynamically
- *Note:* is an extra feature, must be enabled / managed

#### Snapshots
- Can backup data on volumes to [[S3]]
- [[EC2]] instance data & state can be saved
- Restore snapshot on new [[EC2]] instances

#### Multi-Attach
- Attach volumes to multiple instances
- Supported only on some instances types