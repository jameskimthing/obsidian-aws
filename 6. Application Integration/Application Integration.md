#organize 
![[Pasted image 20230405132125.png]]
# Application Integration
- A suite of services that enable communication between:
	- Decoupled components within microservices
	- Distributed systems
	- Serverless applications
- Don’t need to refactor your entire architecture to benefit:
	- Decoupling applications at any scale can reduce the impact of changes, making it easier to update and faster to release new features
- [[Amplify]] --> AWS' Backend-as-a-Service
- [[Step Functions]] --> Coordinate multiple AWS services into serverless workflows so you can build and update apps quickly
- [[Cognito]] --> End-user authentication

## API Management
- REST API: [[API Gateway]]
- GraphQL API: [[AppSync]]

## Event Handling
- [[EventBridge]] --> Event-driven architecture
- [[SNS]] --> Reliable high throughput pub/sub, SMS, email, and mobile push notifications
- [[SQS]] --> Message queue that sends, stores, and receives messages between application components at any volume
- [[Amazon MQ]] --> Message broker for Apache ActiveMQ and RabbitMQ that makes migration easy and enables hybrid architectures

#### Check Differences
|         | [[SQS]]                                              | [[SNS]]                                              | [[EventBridge]]                              |
| ------- | ---------------------------------------------------- | ---------------------------------------------------- | -------------------------------------------- |
| Do      | Push && read messages to the **queue**                   | Push **message directly** to interested subscribers      | **React to all events** & trigger other services |
| About   | Managed *message* (data package) queue service       | Managed *push message* (data package) service        | *Listen to events && trigger* actions        |
| Sync    | Asynchronous processing                              | Synchronous processing                               | Synchronous processing                       |
| Trigger | Directly triggered from inside other services / code | Directly triggered from inside other services / code | Indirectly triggered because of events                                             |



### Problem app integration solves
- *Application A* ----(request)---> to *Application B*
- *B* can expose a web (HTTP) API, built with [[API Gateway]] or [[AppSync]]
- **Problems**
	- Overhead / extra work && costs
	- Same solution must be re-implemented many times
	- Connectivity between apps (& services) could be an issue

