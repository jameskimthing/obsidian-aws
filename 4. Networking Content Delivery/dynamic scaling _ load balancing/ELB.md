# Elastic Load Balancing
![[Elastic Load Balancing.png]]
- Service to distribute load (e.g. incoming requests) evenly across available instances
- Ensures that all available instances are utilized equally
- The 2 main load balancers offered by AWS:
	- ![[Application Load Balancer.png]] **Application Load Balancer** = Feature-rich
		- Broad variety of request forwarding conditions && rules
		- Capable of [[SSL]] Termination
			- Can act as an endpoint for incoming https requests
			- Secure encrypted Https requests can be decrypted here, and forward the un-encrypted requests to other services, like [[EC2]]
			- *Note:* Only termination is possible, use a service like [[ACM]] to manage
		- Can reduce app complexity
		- Use for (most) **HTTP apps**
	- ![[Network Load Balancer.png]] **Network Load Balancer** 
		- Very lean
		- Limited config options
		- Fixed IP address
		- Perfect for non-HTTP traffic
			- e.g. Not running a web server
		- Use for **non-HTTP services**
