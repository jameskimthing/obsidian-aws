#organize 
![[Application Integration.png]]
# Application Integration
- A suite of services that enable communication between:
	- Decoupled components within microservices
	- Distributed systems
	- Serverless applications
- Don’t need to refactor your entire architecture to benefit
- **The Problem App Integration Solves**
	- *Application A* ---> *Application B*
	- *B* can expose a web (HTTP) API, built with [[API Gateway]] or [[AppSync]]
	- **Problems**
		- Overhead / extra work && costs
		- Same solution must be re-implemented many times
		- Connectivity between apps (& services) could be an issue

| Icon | Name | Description |
| --- | --- | --- |
| ![[Amplify.png]] | [[Amplify]] | AWS' Backend-as-a-Service |
| ![[Step Functions.png]] | [[Step Functions]] | Coordinate multiple AWS services into [[Serverless]] workflows |
| ![[Cognito.png]] | [[Cognito]] | End-user authentication |

## API Management

| Icon | Name | Description |
| --- | --- | --- |
| ![[API Gateway.png]] | [[API Gateway]] | REST API |
| ![[AppSync.png]] | [[AppSync]] | GraphQL API |

## Event Handling

| Icon | Name | Description |
| --- | --- | --- |
| ![[SQS.png]] | [[SQS]] | Message queue that sends, stores, and receives messages between application components at any volume |
| ![[SNS.png]] | [[SNS]] | Reliable high throughput pub/sub, SMS, email, mobile push notifications |
| ![[EventBridge.png]] | [[EventBridge]] | Event-driven architecture |
| ![[MQ.png]] | [[MQ]] | Message broker for Apache ActiveMQ and RabbitMQ, that makes migration easy and enables hybrid architectures |

#### Check Differences

|         | [[SQS]]                                              | [[SNS]]                                              | [[EventBridge]]                              |
| ------- | ---------------------------------------------------- | ---------------------------------------------------- | -------------------------------------------- |
| Do      | Push && read messages to the **queue**                   | Push **message directly** to interested subscribers      | **React to all events** & trigger other services |
| About   | Managed *message* (data package) queue service       | Managed *push message* (data package) service        | *Listen to events && trigger* actions        |
| Sync    | Asynchronous processing                              | Synchronous processing                               | Synchronous processing                       |
| Trigger | Directly triggered from inside other services / code | Directly triggered from inside other services / code | Indirectly triggered because of events                                             |





