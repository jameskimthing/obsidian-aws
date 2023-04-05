# Elastic Load Balancing
![[Pasted image 20230405131459.png]]
- Service to distribute load (e.g. incoming requests) evenly across available instances
- Ensures that all available instances are utilized equally
- The 2 main load balancers offered by AWS:
	- ![[Pasted image 20230405131509.png]] **Application Load Balancer** = Feature-rich
		- Broad variety of request forwarding conditions && rules
		- Capable of [[SSL]] Termination
			- Can act as an endpoint for incoming https requests
			- Secure encrypted Https requests can be decrypted here, and forward the un-encrypted requests to other services, like [[EC2]]
			- *Note:* Only termination is possible, use a service like [[ACM]] to manage
		- Can reduce app complexity
		- Use for (most) **HTTP apps**
	- ![[Pasted image 20230405131532.png]] **Network Load Balancer** 
		- Very lean
		- Limited config options
		- Fixed IP address
		- Perfect for non-HTTP traffic
			- e.g. Not running a web server
		- Use for **non-HTTP services**
