# Elastic File System
![[Pasted image 20230405131913.png]]
- Add a (virtual) **file system** without any manual setup
- Can be attached & accessed to / from multiple services
- A scalable, pre-formatted file system
- Create custom structure & store any file (via the command line / code)

# FSx
![[Pasted image 20230405131919.png]]
- (Somtimes) an alternative to **EFS**, but is optimized for high-performance operations
- No feature equality


## abt...
- EFS is cheaper than FSx.
- Some AWS services only support using EFS (AWS Lambda, Linux ECS containers)
- Some AWS services only support using FSx (Windows ECS containers)
