![[VPC.png]]
# Virtual Private Cloud
- Used to manage your own network in the cloud
- Resources are grouped and organized in customer-managed networks
- Has *at least*:
	- 2 [[Subnets]]
	- 1 [[Route Table]]
- Each has a separate *IP CIDR* block (chcek [[IP Addresses]])
	- [[Subnets]] get parts of the block assigned
	- Resources such as an [[EC2]] instance receive auto-assigned public and private IPs
	- *Elastic IP* can be used for a fixed IP address
- [[VPC Endpoint && AWS PrivateLink]] for connecting without the internet

#### Managing Traffic
- Firewalls -> checks incoming / outgoing requests and conditionally blocks / allows them
- Controlling traffic:
	- [[Security Group]] --> At instance level
	- [[NACL]] --> At subnet level
	- *(Security Groups are preferred)*
*Security Groups vs NACL*

| About        | Security Group | Network Access Control List |
| ------------ | ---------------------------------------------------------- | ----------------------------------------------------------------------------- |
| State        | Stateful: Responses are allowed (if the request is passed) | Stateless: Requests & Responses are separate, need to manually allow response |
| Rules        | Supports **allow** rules only                              | Supports **allow && deny** rules                                              |

#### Connection
- for with internal / only with own services, check [[Direct Connect]]

| Icon                      | Name             | Description                                                                                                                                                                 |
| ------------------------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![[Internet Gateway.png]] | Internet Gateway | What makes public [[Subnets]] have access to the internet                                                                                                                   |
| ![[NAT Gateway.png]]      | NAT Gateway      | A Network Address Translation service <br> Instances in a private subnet can connect to the internet <br> External services cannot initiate connection with those instances |
| ![[VPC Peering.png]]      | VPC Peering      | Conecting 2 [[VPC]]s                                                                                                                                                        |
| ![[Transit Gateway.png]]  | Transit Gateway  | Connecting more than 2 [[VPC]]s                                                                                                                                             |
|                           |                  |                                                                                                                                                                             |



#### VPC Endpoint && AWS Privatelink
- Establish connectivity between [[VPC]]s and AWS services without exposing data to the internet
- Check [here](https://stackoverflow.com/questions/66726225/aws-private-link-vs-vpc-endpoint) for more info

| Icon | Name | Description |
| --- | --- | --- |
| ![[VPC Endpoint.png]] | **VPC Endpoint** | The entry point in ur VPC that enables u to connect privately to a service |
| ![[PrivateLink.png]] | **PrivateLink** | A technology that provides private connectivity between VPCs and services |


![[Security Group, NACL.png]]

