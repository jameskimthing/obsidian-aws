# API Gateway
![[Pasted image 20230405132044.png]]
- REST API Service
- Acts as the *front door* for applications to access data, business logic, or functionality from your backend services

#### Usage
- **Define API Structure**
	- Define resources (paths && HTTP methods)
	- Enforce query parameters / authentication
	- Define response codes && schema
- **Handle Requests**
	- Define rules for handling && parsing requests
		- e.g. Automatic parsing
	- Configure response creation && forwarding logic
		- e.g. Gateway --> [[Lambda]] --> Database --> (response from [[Lambda]]) --> Gateway
	- Handle real-time connections (*websockets*)
- **Test && Deploy**
	- Test during development
	- Deploy with stages (versions)


![[API Gateway.png|900]]