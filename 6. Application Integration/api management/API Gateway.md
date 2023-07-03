![[_icons/API Gateway.png]]
# API Gateway
- REST API Service
- Acts as the *front door* for applications to access data, business logic, or functionality from your backend services

![[API Gateway Endpoint.png]]
## Endpoints
- Check [herel](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-api-endpoint-types.html)
- *Edge Optimized API Endpoint* --> **(Default)** utilizes the aws [[Edge Locations]]
	- Best for geographically distributed clients
	- Routed to the nearest CloudFront Point of Presence (POP)
- *Regional API Endpoint* --> Intended for clients of the same region
	- example use cases:
		- When a client running on an [[EC2]] instance calls an API in the same region
		- When an API is intended to serve a small number of clients with high demands
- *Private API Endpoint* --> Ability to have private API endpoints inside your own [[VPC]]
	- Can still use API Gateway features, while:
		- Securely exposing REST APIs only to the other services and resources inside [[VPC]]
		- Onlt to those connected via [[Direct Connect]] to your own data centers

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


![[API Gateway About.png|900]]